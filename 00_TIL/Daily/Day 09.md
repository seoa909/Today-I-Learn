# 여전히 환자.. 하지만 출근..

오늘은 출근 하자마자, 이메일 verify를 하려고 했지만, 갑자기 어제 로컬에 저장해버린 유저 데이터가 신경쓰이기 시작했다.

나에게 필요했던 상황은, 로그인에 성공 후, user 정보를 내려주는데, user정보를 db에서 찾아야하니까 그걸 email로 받아서 내려줬다.

그런데 그 이메일을 받는 방법을 몰라서, 프론트에서 email 정보를 localstorage에 저장했다가, 그걸 토대로 받는 api를 만들었는데,

생각해보니 local에 이런걸 저장하는건 secure하다고 생각이 안들어서 고민을 계속했다.

세화님 남편인 유신님의 깃헙을 계속 보다보니, res.locals를 발견했고, 다른 사람들 깃헙도 보다보니 res.locals 이런 단어가 있길래 공부를 하려는데, 도통 모르겠었다.

그러다가 결국, middleware에서 값을 저장할 수 있는걸 어찌어찌 알게되서, email로 user정보를 찾는게 아니라,

로그인 하면 그 로그인 한 사람의 정보를 내려주는 식으로 서버 코드를 변경했다.


프론트에서는, redux를 사용했었는데, react-query로 변경해서 캐시데이터를 사용하기로 했다 조금 더 안전하게.

그리고 토큰만 localstorage에서 cookie로 저장 위치를 바꿨다.

-------------------------------------

위의 코드만 짜는데 진이 다 빠졌다.. 생각보다 오래걸린거 같다.. 이메일 verify는 nodemailer를 사용하라는데, 힘이없어서 건들지도 못했고, 나머지 힘을 다 쏟아서

타입스크립트에 any를 썼던걸 다 타입으로 변경해 줬다. (못한것도 조금 있다..)

내일은 아마 이메일 verify, 유저정보 변경, 모든 유저보기 정도의 api를 짜고 프론트쪽 까지 작업하지 않을까..

-----------------------------------

오늘은 점심으로 프랭키가 서브웨이 샌드위치를 40개를 사와서 나눠줬다 ㅋㅋㅋ

그리고 뢉이 커피와 도넛을 샀다.

연말이라 그런지 다들 파티 분위기다.

계속 고민인게, 중첩 라우팅을 쓰면, 화면 rerendering이 안되는데, 내가 rerendering이 필요한데.. 이 부분을 프론트에서는 고민하면 될거같다.

(어찌된게 프론트가 더 어렵다 ㅋㅋ.. 진도를 못나간다 ㅋㅋ)

------------------------------

추가로 백재님하고 만드는 이상형 월드컵에서 백재님이 auth 로직에 대해 궁금해 하셔서 알려드리기로 했다.

firebase auth 오랜만이라 기억이.. 일단 storage와 db는 자유롭게 사용 가능하긴해서 이미 월드컵 게임 코드를 그렇게 짜놓기도 했는데,

auth는 조금 걱정이다 ㅋㅋ..
