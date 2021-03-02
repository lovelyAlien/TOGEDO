## TOGEDO!

### 난 네가 오늘 할 일을 알고있다..



> #### [프로젝트명]

- 프로젝트명:  TOGEDO! / 난 네가 오늘 할 일을 알고 있다...

- 기능소개: 
  1. 유저는 오늘 할 일을 작성하여 목록에 등록 할 수 있습니다.
  2. 유저(팀원)들이 작성한 오늘 할 일 목록을 공유합니다.
  3. 특정 유저의 이름을 검색하면 해당 유저의 할 일 목록을 확인 할 수 있습니다.
  4. 프로필 변경을 할 수 있습니다. 



> #### [와이어프레임]

![wireframe](https://user-images.githubusercontent.com/54395509/109492813-dfb58900-7ace-11eb-9e0c-e5616c26d3b6.png)





> #### [API 설계하기]



|              기능               | Method |    URL     |                    request                     |          response          |
| :-----------------------------: | :----: | :--------: | :--------------------------------------------: | :------------------------: |
|            회원가입             |  POST  | /api/login | {'id':id, 'pw':pw, 'name':name, 'email':email} |      회원가입 데이터       |
|             로그인              |  GET   | /api/login |               {'id':id, 'pw':pw}               |       로그인 데이터        |
|           할 일 작성            |  POST  | /api/list  |           {'date':date, 'todo':todo}           |     할 일 작성 데이터      |
|     할 일 리스트 전체 조회      |  GET   | /api/list  |                                                |        할 일 리스트        |
| 검색한 유저의 할 일 리스트 조회 |  GET   | /api/list  |               query={user_name}                | 검색한 유저의 할 일 리스트 |
|                                 |        |            |                                                |                            |





> #### GitHub 주소 

######   https://github.com/lovelyAlien/TOGEDO



