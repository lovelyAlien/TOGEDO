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



|               기능                | Method |                  URL                  |                           request                            |                           response                           |
| :-------------------------------: | :----: | :-----------------------------------: | :----------------------------------------------------------: | :----------------------------------------------------------: |
|         아이디 중복 확인          |  POST  |           /sign_up/check_dup           |                   username_give: username                    |       jsonify({'result': 'success', 'exists': exists})       |
|       회원가입 정보 DB 저장       |  POST  |             /sign_up/save             | {username_give: username, password_give: password, email_give: email} |                jsonify({'result': 'success'})                |
|          로그인 값 입력           |  POST  |               /sign_in                |      {username_give: username,password_give: password}       |        jsonify({'result': 'success', 'token': token})        |
|            프로필 수정            |  POST  |            /update_profile            | form_data =[{"file_give": file}, {"name_give", name}, {"about_give", about}] | jsonify({"result": "success", 'msg': '할 일을 업데이트했습니다.'}) |
|            할 일 등록             |  POST  |              /write_todo              |             {date_give: today, todo_give: todo}              |  jsonify({"result": "success", 'msg': ' 성공'}) |                                                            |
| 검색된 유저의 할 일만 보이게 하기 |  GET   | /get_list?username_give=${username} |                                                              | {"result": "success", "msg": "할 일을 가져왔습니다.", "list": list} |





> #### GitHub 주소 

######   https://github.com/lovelyAlien/TOGEDO
