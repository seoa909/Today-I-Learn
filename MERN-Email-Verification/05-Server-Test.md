# 포스트맨 테스트

- ```http://localhost:5000/api/email``` 여기 api에 post로 본인 이메일, 이름 보내보기
- 샘플
```js
{
    "name": "이름",
    "email": "이메일"
}
```

내가 겪은 에러들 모음

- 에러가 나는데 response에 ```An error occured``` 이런 에러가 반환될때
  - 이건 db에 유저생성이나, 뭐 토큰같은게 들어갈때 나는 에러일 확률이 큼.
  - 그냥 무지성으로 디버깅해야하는데,  ```console.log("첫번째 콘솔")```, ```console.log("두번째 콘솔")```, 이런걸 코드마다 찍어보고 터미널에 어디까지 콘솔이 찍히나 봐야함
  - 그다음에 어느 순간부터 아래로 콘솔이 하나도 안찍히는 순간이 오는데 그럼 거기서부터 파고들면 됌
  - https://github.com/sk-Jahangeer/node-mongo-email-verify 이 깃헙대로하면, 뭘 잘못쓴건지 토큰 컬렉션이 생성이 안되서, 토큰을 그냥 빈 값으로 교체하는 식으로 변경함.

- 에러가 나는데 11000 이런 숫자가 보인다
  - 이건 몽고db에 뭐 중복되는게 있어서 그럼. 그냥 몽고db 전체 컬렉션 날리고 다시 해보는게 빠름
 
- page not found
  - db 연결될때까지 기다리자..