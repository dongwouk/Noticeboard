# 🗒 게시판 만들기

간단히 사용자들과 소통할 수 있는 게시판 서비스입니다. 

## 프로젝트 기능 및 설계
- 회원가입 기능
  - 사용자는 회원가입을 할 수 있다. 일반적으로 모든 사용자는 회원가입시 USER 권한 (일반 권한)을 지닌다.
  - 관리자는 회원가입을 할 수 있다. 일반적으로 관리자는 회원가입시 ADMIN 권한 (관리 권한)을 지닌다.
  - 회원가입시 아이디와 패스워드를 입력받으며, 아이디는 unique 해야한다. 

- 로그인 기능
  - 사용자는 로그인을 할 수 있다. 로그인시 회원가입때 사용한 아이디와 패스워드가 일치해야한다. 

- 게시글 작성 기능 
  - 로그인한 사용자는 권한에 관계 없이 글을 작성할 수 있다. 
  - 사용자는 게시글 제목(텍스트), 게시글 내용(텍스트)를 작성할 수 있다.

- 게시글 수정 기능
  - 로그인한 사용자는 자신이 작성한 게시글을 수정할 수 있다.
  - 사용자는 게시글 제목과 게시글 내용을 수정할 수 있으며, 수정된 시간은 저장된다.

- 게시글 목록 조회 기능 
  - 로그인하지 않은 사용자를 포함한 모든 사용자는 게시글을 조회할 수 있다. 
  - 게시글은 최신순으로 기본 정렬되며, 댓글이 많은순/적은순 으로도 정렬이 가능하다.
  - 게시글 목록 조회시 응답에는 게시글 제목과 작성일, 댓글 수의 정보가 필요하다.
  - 게시글은 종류가 많을수 있으므로 paging 처리를 한다. 

- 특정 게시글 조회 기능
  - 로그인하지 않은 사용자를 포함한 모든 사용자는 게시글을 조회할 수 있다. 
  - 게시글 제목, 게시글 내용, 작성자, 작성일이 조회된다. 

- 댓글 목록 조회 기능
  - 특정 게시글 조회시 댓글목록도 함께 조회가 된다. 다만 댓글은 많을 수 있기 때문에 별도의 API로 구성한다. 이 또한 로그인하지 않은 사용자를 포함한 모든 사용자가 댓글을 조회할 수 있다.
  - 댓글은 최신순으로만 정렬되며, paging 처리를 한다. 
  - 댓글 목록 조회시에는 댓글 작성자와 댓글 내용, 댓글 작성일의 정보가 필요하다.

- 댓글 작성 기능
  - 로그인한 사용자는 권한에 관계 없이 댓글을 작성할 수 있다. 
  - 사용자는 댓글 내용(텍스트)를 작성할 수 있다.
  
- 게시글 삭제 기능
  - 관리자는 부적절하거나 규칙을 위반한 게시글을 삭제할 수 있습니다.

- 댓글 삭제 기능
  - 관리자는 부적절한 댓글을 삭제할 수 있습니다.


## ERD 
![ERD](doc/img/notice.png)

## Trouble Shooting
[go to the trouble shooting section](doc/TROUBLE_SHOOTING.md)

### Tech Stack
<div align=center> 
<img src="https://img.shields.io/badge/Java-59666C?style=for-the-badge&logo=Spring&logoColor=white"/>
<img src="https://img.shields.io/badge/SpringBoot-59666C?style=for-the-badge&logo=SpringBoot&logoColor=white"/>
<img src="https://img.shields.io/badge/Spring Security-59666C?style=for-the-badge&logo=Spring Security&logoColor=white"/>
<img src="https://img.shields.io/badge/gradle-59666C?style=for-the-badge&logo=gradle&logoColor=white"/>
<img src="https://img.shields.io/badge/Lombok-59666C?style=for-the-badge&logo=Spring&logoColor=white"/>
<img src="https://img.shields.io/badge/Mysql-59666C?style=for-the-badge&logo=MySql&logoColor=white"/>
<img src="https://img.shields.io/badge/git-59666C?style=for-the-badge&logo=git&logoColor=white">
</div>
