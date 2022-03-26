# semi_implement


## 🔨 자유 게시판 - 기능 상세 소개

### 구성
1. [전체 게시글 조회](#전체-게시글-조회)

2. [게시물 정렬 조회](#게시물-정렬-조회)

3. [게시물 검색](#게시물-검색)

4. [게시물 카테고리별 조회](#게시물-카테고리별-조회)

5. [게시물 작성](#게시물-작성)

6. [게시물 상세보기 및 수정삭제](#게시물-상세보기-및-수정삭제)

7. [게시물 좋아요 및 북마크](#게시물-좋아요-및-북마크)

8. [게시글에 대한 댓글](#게시글에-대한-댓글)

9. [댓글 정렬](#댓글-정렬)


### 사용 스택
 
  
<img src="https://img.shields.io/badge/JAVA-007396?style=for-the-badge&logo=java&logoColor=white"> <img src="https://img.shields.io/badge/Spring-6DB33F?style=for-the-badge&logo=Spring&logoColor=white"> <img src="https://img.shields.io/badge/mysql-4479A1?style=for-the-badge&logo=mysql&logoColor=white"> <img src="https://img.shields.io/badge/javascript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black"> <img src="https://img.shields.io/badge/jquery-0769AD?style=for-the-badge&logo=jquery&logoColor=white"> <img src="https://img.shields.io/badge/github-181717?style=for-the-badge&logo=github&logoColor=white">

### 전체 게시글 조회
### (Infinite Scroll) 
![무한스크롤](https://user-images.githubusercontent.com/100342241/160203246-4a63ced2-f85b-400d-b288-c3a6b2777043.gif)
- 화면을 스크롤하면 게시물이 하단에 10개씩 나타납니다
- 스크롤을 바닥까지 내리면 ajax를 통해 화면 전환없이 다음 페이지 정보를 요청하고,<br> 그 응답을 다른 jsp파일에 실어 보낸 후 붙여주는 방식으로 구현하였습니다.
- [JSP 코드보기 Click! :monocle_face:](https://github.com/jayPark14/team1/blob/main/semiproject_team1/src/main/webapp/WEB-INF/views/board/boardForm_all.jsp)
- [Controller 코드보기 Click! 🔍️](https://github.com/jayPark14/team1/blob/main/semiproject_team1/src/main/java/com/semi/controller/Board_allController.java)
<br><br>

### 게시물 정렬 조회
![게시물정렬](https://user-images.githubusercontent.com/100342241/160195017-78b62831-a7cb-4e6a-af34-c4920f27a74d.gif)
- 정렬 조건에 맞는 게시물을 10개씩 가져옵니다
- [Controller 코드보기 Click! 🔍️](https://github.com/jayPark14/team1/blob/main/semiproject_team1/src/main/java/com/semi/controller/Board_allController.java)<br><br>

### 게시물 검색
![검색](https://user-images.githubusercontent.com/100342241/160194435-e13dd04f-6012-49ce-a940-a6c40195f1cf.gif)
- 선택한 분류에 검색어가 포함된 게시물을 가져옵니다
- [Controller 코드보기 Click! 🔍️](https://github.com/jayPark14/team1/blob/main/semiproject_team1/src/main/java/com/semi/controller/Board_allController.java)
<br><br>

### 게시물 카테고리별 조회
![카테고리](https://user-images.githubusercontent.com/100342241/160195724-bb7542a4-aa03-473f-a34d-2bf38d291eec.gif)
- 좌측 메뉴바에서 원하는 카테고리를 선택하면 동일한 카테고리의 게시물만 나타납니다
 - [전체 Controller 코드보기 Click! 🔍️](https://github.com/jayPark14/team1/blob/main/semiproject_team1/src/main/java/com/semi/controller/Board_allController.java)
 - [하이라이트 Controller 코드보기 Click! 🔍️](https://github.com/jayPark14/team1/blob/main/semiproject_team1/src/main/java/com/semi/controller/Board_highlightController.java)
 - [자유 Controller 코드보기 Click! 🔍️](https://github.com/jayPark14/team1/blob/main/semiproject_team1/src/main/java/com/semi/controller/Board_normalController.java)
 - [팁과 노하우 Controller 코드보기 Click! 🔍️](https://github.com/jayPark14/team1/blob/main/semiproject_team1/src/main/java/com/semi/controller/Board_tipController.java)
<br><br>

### 게시물 작성
![게시물작성](https://user-images.githubusercontent.com/100342241/160208303-f023fc50-d52b-46fb-8a06-11a59bc6d0b1.gif)
- 게시물 작성버튼을 누르면 게시물 작성 양식으로 이동되고, 유효성 검사를 통과할경우 게시물이 등록되어 자유게시판 화면에 나타납니다.
- 동영상, 사진의 경우 선택사항에 해당하며 사진을 등록시 해당 게시글의 썸네일이 나타납니다.
- [JSP 코드보기 Click! :monocle_face:](https://github.com/jayPark14/team1/blob/main/semiproject_team1/src/main/webapp/WEB-INF/views/board/boardwriteForm.jsp)
- [Controller 코드보기 Click! 🔍️](https://github.com/jayPark14/team1/blob/main/semiproject_team1/src/main/java/com/semi/controller/Board_allController.java)
<br><br>

### 게시물 상세보기 및 수정삭제
![수정삭제](https://user-images.githubusercontent.com/100342241/160208289-b85a2974-bc58-4672-97db-a9f3d410bb73.gif)
- 게시물을 누를 경우 상세보기로 이동하며, 게시물의 수정 및 삭제가 가능합니다
- [JSP 상세보기 코드보기 Click! :monocle_face:](https://github.com/jayPark14/team1/blob/main/semiproject_team1/src/main/webapp/WEB-INF/views/board/boardDetail.jsp)
- [JSP 수정 코드보기 Click! :monocle_face:](https://github.com/jayPark14/team1/blob/main/semiproject_team1/src/main/webapp/WEB-INF/views/board/modifyForm.jsp)
- [Controller 코드보기 Click! 🔍️](https://github.com/jayPark14/team1/blob/main/semiproject_team1/src/main/java/com/semi/controller/Board_allController.java)
<br><br>

### 게시물 좋아요 및 북마크
![좋아요북마크](https://user-images.githubusercontent.com/100342241/160207278-c234a381-7ff7-4427-8d69-d03e9d381fba.gif)
- 게시물의 좋아요를 누를 경우 해당 게시물의 좋아요 숫자가 증가하고, 북마크를 누를 경우 누른 유저의 마이페이지에서 게시물의 확인 및 상세보기가 가능합니다.
- [JSP 상세보기 코드보기 Click! :monocle_face:](https://github.com/jayPark14/team1/blob/main/semiproject_team1/src/main/webapp/WEB-INF/views/board/boardDetail.jsp)
- [Controller 코드보기 Click! 🔍️](https://github.com/jayPark14/team1/blob/main/semiproject_team1/src/main/java/com/semi/controller/Board_allController.java)
<br><br>

### 게시글에 대한 댓글
![댓글기능1](https://user-images.githubusercontent.com/100342241/160207898-98c977bb-6e19-4597-880a-f84a8439e865.gif)
- 댓글 및 대댓글을 등록, 삭제 가능하도록 구현하였습니다
- [JSP 상세보기 코드보기 Click! :monocle_face:](https://github.com/jayPark14/team1/blob/main/semiproject_team1/src/main/webapp/WEB-INF/views/board/boardDetail.jsp)
- [Controller 코드보기 Click! 🔍️](https://github.com/jayPark14/team1/blob/main/semiproject_team1/src/main/java/com/semi/controller/Board_allController.java)
<br><br>

### 댓글 정렬
![댓글기능2](https://user-images.githubusercontent.com/100342241/160195580-4b80f88d-8bb4-4da4-b65e-556c6d55f6aa.gif)
- 댓글에 좋아요를 누를고 취소할 수 있고, 최신 및 인기순으로 댓글 정렬이 가능합니다
- [JSP 상세보기 코드보기 Click! :monocle_face:](https://github.com/jayPark14/team1/blob/main/semiproject_team1/src/main/webapp/WEB-INF/views/board/boardDetail.jsp)
- [Controller 코드보기 Click! 🔍️](https://github.com/jayPark14/team1/blob/main/semiproject_team1/src/main/java/com/semi/controller/Board_allController.java)


