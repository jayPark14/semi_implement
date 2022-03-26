
# semi_implement


## 🔨 피드백 게시판 - 기능 상세 소개

### 구성
1. [전체 피드백 조회](#전체-피드백-조회)

2. [피드백 요청 게시물 정렬](#피드백-요청-게시물-정렬)

3. [피드백 요청 게시물 검색](#피드백-요청-게시물-검색)

4. [피드백 요청 게시물 작성](#피드백-요청-게시물-작성)

5. [피드백 요청 게시물에 대한 피드백 답변](#피드백-요청-게시물에-대한-피드백-답변)

6. [피드백 답변 선택](#피드백-답변-선택)


### 사용 스택
 
  
<img src="https://img.shields.io/badge/JAVA-007396?style=for-the-badge&logo=java&logoColor=white"> <img src="https://img.shields.io/badge/Spring-6DB33F?style=for-the-badge&logo=Spring&logoColor=white"> <img src="https://img.shields.io/badge/mysql-4479A1?style=for-the-badge&logo=mysql&logoColor=white"> <img src="https://img.shields.io/badge/javascript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black"> <img src="https://img.shields.io/badge/jquery-0769AD?style=for-the-badge&logo=jquery&logoColor=white"> <img src="https://img.shields.io/badge/github-181717?style=for-the-badge&logo=github&logoColor=white">

### 전체 피드백 조회
### (Infinite Scroll) 
![무한스크롤](https://user-images.githubusercontent.com/100342241/160211654-708c902b-6481-4fa1-876b-5b4cc1075972.gif)
- 자유게시판과 동일하게 화면을 스크롤하면 게시물이 하단에 10개씩 나타납니다
- 스크롤을 바닥까지 내리면 ajax를 통해 화면 전환없이 다음 페이지 정보를 요청하고,<br> 그 응답을 다른 jsp파일에 실어 보낸 후 붙여주는 방식으로 구현하였습니다.
- [JSP 코드보기 Click! :monocle_face:](https://github.com/jayPark14/team1/blob/main/semiproject_team1/src/main/webapp/WEB-INF/views/feedback/feedbackForm.jsp)
- [Controller 코드보기 Click! 🔍️](https://github.com/jayPark14/team1/blob/main/semiproject_team1/src/main/java/com/semi/controller/FeedbackController.java)
<br><br>
<br><br>

### 피드백 요청 게시물 정렬
![정렬](https://user-images.githubusercontent.com/100342241/160212179-1bcfc447-15d5-4204-a1ed-a6efad8a48bf.gif)
- 자유게시판과 동일하게 정렬 조건에 맞는 게시물을 10개씩 가져옵니다
- [JSP 코드보기 Click! :monocle_face:](https://github.com/jayPark14/team1/blob/main/semiproject_team1/src/main/webapp/WEB-INF/views/feedback/feedbackForm.jsp)
- [Controller 코드보기 Click! 🔍️](https://github.com/jayPark14/team1/blob/main/semiproject_team1/src/main/java/com/semi/controller/FeedbackController.java)
<br><br>

### 피드백 요청 게시물 검색
![검색](https://user-images.githubusercontent.com/100342241/160211670-26c5fd58-f44b-4c36-993a-a063513760e1.gif)
- 자유게시판과 동일하게 선택한 분류에 검색어가 포함된 게시물을 가져옵니다
- [JSP 코드보기 Click! :monocle_face:](https://github.com/jayPark14/team1/blob/main/semiproject_team1/src/main/webapp/WEB-INF/views/feedback/feedbackForm.jsp)
- [Controller 코드보기 Click! 🔍️](https://github.com/jayPark14/team1/blob/main/semiproject_team1/src/main/java/com/semi/controller/FeedbackController.java)
<br><br>

### 피드백 요청 게시물 작성
![피드백요청](https://user-images.githubusercontent.com/100342241/160211682-b4e419ad-1837-498a-a6ea-2b089f8d34be.gif)
- 피드백 요청 버튼을 눌러 자신의 플레이에 대한 피드백을 다수의 사용자들에게 요청할 수 있습니다
- 피드백 요청 게시물을 작성하기 위해서는 리플레이 파일, 게임 플레이 영상이 필수적으로 포함되어야 하며 자유게시판과 동일하게 사진은 선택할 수 있습니다
- [JSP 코드보기 Click! :monocle_face:](https://github.com/jayPark14/team1/blob/main/semiproject_team1/src/main/webapp/WEB-INF/views/feedback/feedbackwriteForm.jsp)
- [Controller 코드보기 Click! 🔍️](https://github.com/jayPark14/team1/blob/main/semiproject_team1/src/main/java/com/semi/controller/FeedbackController.java)
<br><br>

### 피드백 요청 게시물에 대한 피드백 답변
https://user-images.githubusercontent.com/100342241/160211439-d7b2d2a1-b1b1-4673-8668-238ce15a84dc.mp4
- 피드백 요청 게시물에 대해 피드백 답변을 작성할 수 있습니다.
- [JSP 코드보기 Click! :monocle_face:](https://github.com/jayPark14/team1/blob/main/semiproject_team1/src/main/webapp/WEB-INF/views/feedback/feedbackDetail.jsp)
- [Controller 코드보기 Click! 🔍️](https://github.com/jayPark14/team1/blob/main/semiproject_team1/src/main/java/com/semi/controller/FeedbackController.java)

<br><br>

### 피드백 답변 선택

https://user-images.githubusercontent.com/100342241/160211455-66a0ec0b-500c-4525-b594-a5f24d4d3d32.mp4
- 피드백 답변은 우선적으로 좋아요를 가장 많이 받은 순으로 정렬되고, 다음으로는 최신순으로 정렬됩니다.
- 피드백 요청자가 등록된 피드백 답변들을 고정시킬 경우 최상단에 위치하게 되며. 피드백 답변자의 등급 점수가 10점 상승됩니다.
- [JSP 코드보기 Click! :monocle_face:](https://github.com/jayPark14/team1/blob/main/semiproject_team1/src/main/webapp/WEB-INF/views/feedback/feedbackDetail.jsp)
- [Controller 코드보기 Click! 🔍️](https://github.com/jayPark14/team1/blob/main/semiproject_team1/src/main/java/com/semi/controller/FeedbackController.java)

<br><br>



