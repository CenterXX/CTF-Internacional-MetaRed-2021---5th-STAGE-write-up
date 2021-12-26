# Vulns? None
- Category : WEB
- Author : randN

<hr>

# Solve

이 문제는 매우 간단했습니다 
일단 쿠키값에서 JWT 토큰값을 발견했습니다.

사이트로는 ```https://jwt.io/``` 를 사용하였습니다.
- 우선 JWT 토큰을 디코드해 정보를 얻어냈습니다 
<img width="500" src="https://user-images.githubusercontent.com/90122834/147406429-424965ca-45ce-400e-9bcb-8f1f2befbca3.png">

얻어 낸 값으로는
- 토큰의 값은 JWT
- 토큰 검증을 위한 signature에 사용될 알고리즘은 RS256
-  시그니쳐 검증을 위한 키 값을 확인할 수 있었습니다


이를 토대로 간단한 파이썬 코드를 짜서 플래그를 획득 할 수 있었습니다 

하지만 이 방법 말고도 다른 방법으로도 해결해봤습니다

회원가입을 할수있는 창이 있었는데 ```id : admin password : 1```을 통해서 가입후 

admin page로 acces시 플래그를 획득 할 수 있었습니다

flag : ```CTFUA{JWT_1337_N0n3_dnVsbg==}```


