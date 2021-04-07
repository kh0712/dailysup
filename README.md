
<h1>Dailysup</h1>
<h3>Alarm Service to Change Daily Supplements </h3>
<p>Clone coding and refactoring for study from scratch</p>
<p>Original Project: https://github.com/mash-up-kr/Tich-Backend</p>

<div>
    <p>it is not for commercial purpose</p>
    <p>ignored credential(yml, jwt, aws properties)</p>

    What are used: spring boot mvc and security,
                   jwt, spring data jpa, aws s3 and deployed in ec2

Every request except sign-up and log-in needs <br/>
jwt token starting with "Bearer: " in "Authorization" header. 

</div>

<hr>
<p>everything will be changed according to this:<br> 
<a href="https://stackoverflow.blog/2020/03/02/best-practices-for-rest-api-design/">best restful practice</a>

<br><br>

<Strong> ---Invalid Api Doc---(수정중)</Strong>

<h3> Account </h3>

/api/account/

|url|method|desc|
|---|---|---|
|current|get|토큰 계정의 정보를 가져온다.|
|sign-up|post|회원가입을 요청한다.|
|log-in|post|토큰을 발급받는다.|
|withdraw|post|회원 탈퇴한다.|
|email|post|이메일을 변경한다.|
|password|post|비밀번호를 변경한다.|
|profile|get|프로필 사진을 조회한다.|
|profile|post|프로필 사진을 변경한다.|

<br/><br/>

<h3>Item</h3>

/api/item/

|url|method|desc|
|---|---|---|
| |get|토큰 계정의 아이템 목록을 가져온다.|
|{itemId}|get|해당 id의 아이템 정보를 가져온다.|
|{itemId}|post|아이템의 정보를 수정한다.|
|update/{itemId}|post|아이템의 교체일을 갱신한다.|
|{itemId}|delete|아이템을 삭제한다.|
|picture/{itemId}|get|아이템의 사진을 가져온다.|
|picture/{itemId}|post|아이템의 사진을 교체한다.|

<br/><br/>
<h3>History</h3>

/api/history/

|url|method|desc|
|---|---|---|
|{itemId}|get|아이템의 교체 기록을 가져온다.|
| |put|아이템 교체 기록을 수정한다.|
|{historyId}|delete|교체 기록을 삭제한다.|

<br/><br/>
<h3>Device</h3>

/api/device/

|url|method|desc|
|---|---|---|
| |get|토큰 계정의 디바이스 목록을 가져온다.|
| |post|토큰 계정에 디바이스를 등록한다.|
| |delete|디바이스를 삭제한다.(fcm 토큰은 body에 담긴다.)|
|all|delete|토큰 계정의 디바이스 모두 삭제한다.|



