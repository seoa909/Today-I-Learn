# 알고리즘에 질린 하루..

오늘은 샤피파이에서 데이터를 fetching 해야하는데,

샤피파이는 한번에 최대 250개의 데이터만 fetching하도록 막아놨다 (그것마저 프론트에서 fetching하면 CORS나고, 무조건 백에서 해야한다..)

그래서 뭐.. 결국 백에서 받아냈다.

중요한건 한번에 250개의 데이터밖에 안들어오고 headers에 link라는곳에 <html> 태그로 다음페이지를준다.

이 부분은 오후 내내 알고리즘을 짜고 짜서 결국 만들어냈다.
  
우리 신입은 계속 무언가를 나에게 보여주려고 하는데, 글쎄.. 열심히는 하는거 같은데, 일단은 성과는 아직 미비하고 그냥 지켜볼려고한다.
  
아직은 자바스크립트의 배열 method나 string method 이런것들이랑 친해지도록 내비려 둘까 한다. 물론 리액트와 노드도.
  
----------------------------------------
  
그 외에는 할만이 13만개의 데이터를 차트화 해야하는데 죽을맛이라고 했고.. 뭐 별거 없던 하루다.

오늘 그래도 4천개 데이터 카테고라이징까지 끝났으니까, 이제 화면에서 어떻게 보여줄지만 구상하면 이번주도 무난히 끝날거같다.