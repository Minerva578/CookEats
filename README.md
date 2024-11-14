# <CooEats : 공공데이터 활용 레시피 검색 및 공유 웹 사이트>
### Springboot와 JSP & ThymeLeaf를 사용한 웹사이트 제작
&nbsp; 
![image](https://github.com/user-attachments/assets/a14c1167-e7bb-4654-bb62-630274bb2a26)

&nbsp;
### 목차
1. 프로젝트 개요
2. 구성원 및 맡은 역할
3. 서비스 환경
4. 사용 라이브러리 및 외부 API
5. 사이트 맵 (유저, 관리자)
6. 주요 기능
7. ERD 다이어그램
&nbsp; &nbsp;&nbsp;
## 1️. 프로젝트 개요
### (1) 프로젝트 주제 및 목적
## 음식 레시피 검색 및 레시피 공유 사이트
&nbsp; 
## 2️. 구성원 및 맡은 역할
|이름|역할|맡은 역할|
|------|---|---|
|고혜정|팀장| 프로젝트 총괄 및 팀장, 레시피 검색 기능, 회원가입, 로그인 기능, KaKao MAP 장소 표시기능 구현  |
|김현주|팀원| 자유 게시판 CRUD, 검색 & 정렬 기능 구현, 댓글 CRUD 구현, 좋아요 기능, 조회수 기능 구현 |
|윤지훈|팀원| 공공데이터 포털 레시피 API를 통한 DB 저장, 이미지 파일 업로드 기능, 레시피 게시판 CRD 구현|
|전명세|팀원| 장터 게시판 CRUD, 검색 & 정렬 기능 구현, 댓글 CRUD 구현, 좋아요 기능, 조회수 기능 구현|

## 3️. Skills
| 구분                          |    내용                                                                                          | 비고|
|-------------------------------|----------------------------------------------------------------------------------------------------|-------------|
| Languages   | [![My Skills](https://skillicons.dev/icons?i=java,js,html,css,&theme=light)](https://skillicons.dev)| JPA & ThymeLeaf |
| FrameWork   | [![My Skills](https://skillicons.dev/icons?i=spring&theme=light)](https://skillicons.dev)|
| OS   | [![My Skills](https://skillicons.dev/icons?i=linux&theme=light)](https://skillicons.dev)|
| DB   | [![My Skills](https://skillicons.dev/icons?i=mysql&theme=light)](https://skillicons.dev)|
|Cloud|[![My Skills](https://skillicons.dev/icons?i=aws&theme=light)](https://skillicons.dev)|
|IDE|[![My Skills](https://skillicons.dev/icons?i=idea,vscode&theme=light)](https://skillicons.dev)|
|Collaboration|[![My Skills](https://skillicons.dev/icons?i=git,github&theme=light)](https://skillicons.dev)|
|Communication|[![My Skills](https://skillicons.dev/icons?i=notion&theme=light)](https://skillicons.dev)|

## 4. 사용 라이브러리 및 외부 API
### (1) 사용 라이브러리
| 라이브러리 명 | 버전 | 용도 |
|---------------|-------|------------------------------------------|
| AWS Java SDK | 1.12.770 | AWS 서비스와의 연동을 위한 Java SDK 제공 |
| Lombok | 최신 버전 사용 | 어노테이션을 통한 코드 간결화와 편의성 제공 |
| JUnit Platform Launcher | 최신 버전 사용 | JUnit 테스트 프레임워크 실행을 위한 런처 |
| Kakao Maps JavaScript SDK | 최신 버전 사용 | 카카오 지도 API를 이용한 지도 및 위치 기반 서비스 제공 |
| MySQL Connector J | 최신 버전 사용 | Java와 MySQL 데이터베이스 연결 |
| Spring Boot Starter | 3.2.8 | Spring Boot의 핵심 의존성 모음 |
| Spring Boot Starter Logging | 3.2.8 | 기본적인 로깅 기능 제공 |
| Spring Boot Starter WebFlux | 3.2.8 | 반응형 웹 애플리케이션과 비동기 이벤트 스트림 제공 |
| Spring Boot Starter OAuth2 Client | 3.2.8 | OAuth2 및 OpenID Connect 클라이언트 기능 제공 |
| Spring Boot Starter Security | 3.2.8 | 인증과 권한 관리를 위한 보안 기능 제공 |
| Spring Boot Starter Data JPA | 3.2.8 | Spring Data JPA를 활용한 데이터베이스 작업 및 CRUD 기능 제공 |
| Spring Boot Starter Web | 3.2.8 | 웹 애플리케이션의 기본 구조 제공, RESTful 웹 서비스 구축 |
| Spring Boot Starter Thymeleaf | 3.2.8 | Spring Boot와 Thymeleaf를 연결하여 서버 사이드 렌더링 제공 |
| Spring Boot DevTools | 최신 버전 사용 | 개발 시 자동 리로딩을 통한 생산성 향상 |
| Spring Security Test | 최신 버전 사용 | 보안 기능에 대한 테스트 편의성 제공 |
| Thymeleaf Extras Spring Security 6 | 최신 버전 사용 | Thymeleaf 템플릿에서 Spring Security 기능을 쉽게 사용할 수 있도록 지원 |

### (2) 사용 외부 API
| 기능         | API 명             | 제공        | 용도                            |
|--------------|--------------------|-------------|---------------------------------|
| 게시판       | 카카오 맵          | Kakao Developers | 거래장소 위치 표시를 위한 기능 |
| 레시피 게시판 | 공공데이터 포털    | 공공데이터 포털 | 레시피 관련 정보 제공을 위한 기능 |

## 5️. ERD 다이어그램
![image](https://github.com/user-attachments/assets/500daa82-72c3-4914-aac0-c25cacaa294b)

## 6. 주요 기능 및 화면 소개 &nbsp;
### 1. 사용자
#### (1) 로그인 및 회원가입
![image](https://github.com/user-attachments/assets/86add1d3-fa78-429c-8b9e-2bb0d5bc7858)
![image](https://github.com/user-attachments/assets/4a5911cc-a15b-4d29-9c64-7e154179198c)

#### (2) 메인 화면 (검색)
![image](https://github.com/user-attachments/assets/7f80bc62-67be-4bb6-bb1b-06ab70124158)

#### (3) 레시피 추천
![image](https://github.com/user-attachments/assets/c39cb1c1-98b6-4060-b09e-1c3d8a8a950e)

#### (4) 장터 게시판 (목록)
![image](https://github.com/user-attachments/assets/e756e37b-9ac0-4796-8d86-69b6a4715958)

#### (5) 장터 게시판 (게시글 디테일 & 댓글, 게시글 작성)
![image](https://github.com/user-attachments/assets/661c5c78-3940-4ed5-9b11-1eb1b54c026b)
![image](https://github.com/user-attachments/assets/7120ff87-8654-4105-86ef-bcd3c130c3aa)
![image](https://github.com/user-attachments/assets/603d539f-d1ec-413f-9d92-dccfd3b532df)

#### (6) 장터 게시판 (게시글 수정)
![image](https://github.com/user-attachments/assets/bf255048-408c-4f96-82ab-bd45690fe548)

#### (7) 자유 게시판 (목록)
![image](https://github.com/user-attachments/assets/f3af6914-3f90-4b76-88b0-4a27a72b9bcb)

#### (8) 자유 게시판 (게시글 디테일 & 댓글, 게시글 작성)
![image](https://github.com/user-attachments/assets/21f815a7-7892-41ae-ae0a-2d85cc737f49)
![image](https://github.com/user-attachments/assets/b2fc2ede-cd21-43fd-ada5-c6045f1b37aa)

#### (9) 자유 게시판 (게시글 수정)
![image](https://github.com/user-attachments/assets/0a75b920-de78-4347-a4ca-c9666401e8e8)

#### (10) 레시피 게시판 (목록)
![image](https://github.com/user-attachments/assets/958a4887-fd8c-41e3-acd1-eb1b8ccba645)

#### (11) 레시피 게시판 (게시글 디테일 & 댓글, 게시글 작성)
![image](https://github.com/user-attachments/assets/1eb8cf33-f110-43e7-974b-6cd114727afd)
![image](https://github.com/user-attachments/assets/d3ad82d9-b976-4cb3-9dd7-7b434f10fd64)
![image](https://github.com/user-attachments/assets/1d555588-3619-4764-be65-817076389986)
