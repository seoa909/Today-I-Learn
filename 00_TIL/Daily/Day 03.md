# 오늘도 혼자.

딱히 할게없어서 만든 내 Monday..

![aa](https://user-images.githubusercontent.com/59503331/207721042-953ec370-5005-4ee7-beda-41463d33fce8.PNG)

오늘 결국 만든건 헤더에 프로필 사진 추가될 공간 하나 밖에 없다.

실은 dropdown을 만들다가 실패해서 결과물이 없다.

dropdown을 만들어야하는데, 이게 category안에 subcategory가 열리는 방식으로 해야하는데

거기에 NavLink도 같이 추가해줘야한다.

-------------

1차 시도:

NavLink를 안쓰고 꼼수를 통해 url을 가져와서 거기 카테고리면 div 생성으로 삼항연산자를 사용.

결과: 재사용성이 거의 불가능하고, 뭔가 성에 안차서 삭제.

-------------

2차 시도:

NavLink를 사용해서 새로운 dropbox제작, 

결과: useState로 만들었는데, 처음에 isOpen을 false값을 주면, 해당 카테고리를 두번 눌러야지 드랍다운이 열리는 현상

이유: 처음 누르면 KPI page가 열린다 (false), 거기서 한번 더 누르면 그제서야 true로 바뀐다. 

뭐 결과적으로는 지웠다.

-------------

로직을 조금 더 고민해 봐야할거같아서, 일단 오늘은 무리인거같기도하고 해서 노드 공부를 했다.

노드 생각보다 쉬웠다.

오늘은 인터넷에 돌아다니는 자료들을 이것저것 참고해서 내 몽고db 컬렉션에 회원가입 쿼리를 보내는거 까지 성공했다. 

내일 공부는 아마 이제 MERN을 할거같다. 간단한 todo 정도를 만들어 볼까한다. 

-------------

회사에서는 롭이 제일 말 잘 걸어준다.. 이름도 부르면서 인사도 해주고.. 나머지는 바쁘다 ㅜ 

나도 말을 걸고싶은데, 뭐라 걸지도 모르겠다. 너무 집에서만 일을했나..

오늘은 나를 뽑는데 한표 기여했다는 린자라는 사람하고 얘기를 좀 했다. 내이름을 알길에 너 내이름 어케아냐고 물어보니,

내가 너 뽑을때 거기에 컨펌 내리사람중 한명이야~ ,,, 높은사람이었던거같다 물류팀연구원이던데 회사에 한명뿐인 인재.

이제 3일차인데, 그래도 어느정도 여유가 생기고 적응을 해가는게 느껴져서 뭔가 마음이 편하다.

----------------

추가로 오늘 Ks' Castle 을 만들었다.

좋은 분과 프로젝트들을 계속 만들어 가는 공간인 만큼, 도움도 드리고 도움도 받으면서 같이 재밌게 작업해야겠다.