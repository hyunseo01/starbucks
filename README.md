스타벅스 클론코딩 프로젝트

1. 개요:
   - React와 Spring Boot를 활용한 스타벅스 코리아 클론 코딩. 사용자 페이지와 관리자 페이지로 구성되며, 데이터는 MySQL을 통해 관리.
   - frontend: React, Next.js로 사용자 및 관리자 페이지를 구현.
   - backend: Spring Boot로 데이터 처리 및 API 제공.

2. 기술 스택:
   - 프론트엔드: HTML, CSS, JS, TS, React, Next.js
   - 백엔드: Java, Spring Boot, JPA, Lombok, MySQL.
   - @RestController의 매핑 주소와 라우터의 주소가 동일하게 설계(중요)

3. React (frontend):
   - React Router로 사용자 페이지(/starbucks)와 관리자 페이지(/admin) 분리.
   - 이미지 파일은 public/images에 저장, 파일명만 데이터베이스에 저장.

4. Spring Boot (backend):
   - @RestController로 API 제공 (/, /starbucks, /starbucks/coffee, /starbucks/coffee/findall.do(전체 출력 페이지), /starbucks/coffee/find.do/coffeeno=? (커피 개별 페이지)).
   - @RestController의 매핑 주소와 라우터의 주소가 동일하게 설계
   - MySQL 연동 및 JSON 데이터 반환.
   - Lombok으로 코드 간소화.

5. 데이터 흐름:
   - React는 Node.js(5000)에서 실행.
   - React가 백엔드(Spring Boot, 8080)에서 데이터 요청.
   - Spring Boot는 데이터를 처리해 JSON으로 응답.

6. GitHub Pages 배포:
   - 프론트엔드만 배포.
   - 백엔드는 로컬에서 실행하여 연동.

7. 관리자 페이지:
   - React에서 /admin 경로로 관리자 페이지 구현.
   - API를 통해 메뉴 추가/수정/삭제 기능 지원.

8. 서버 기본 상식
- 서버: 데이터를 처리하고 요청을 응답하는 역할.
- HTTP: 프론트엔드와 백엔드가 데이터를 주고받을 때 사용하는 프로토콜.
  - 프론트엔드는 요청(Request)을 보내고, 백엔드는 응답(Response)을 돌려줌.
  - 요청 방식(메서드):
    - GET: 데이터를 가져오기.
    - POST: 데이터를 추가하기.
    - PUT: 데이터를 수정하기.
    - DELETE: 데이터를 삭제하기.
- REST API: 데이터를 주고받기 위해 정해진 규칙에 따라 설계된 URL과 메서드의 집합.
- 데이터 흐름:
    1) React(프론트엔드)에서 API를 호출하여 데이터를 서버에서 가져옴.
    2) React는 가져온 데이터를 화면에 렌더링.
    3) 사용자가 관리자 페이지에서 데이터를 수정하면, 수정 내용을 백엔드(Spring Boot)에 보내 API로 처리.
    4) 데이터는 MySQL 데이터베이스에 저장됨.
 - 프로젝트 하면서 알아야할 서버관련 내용
   - API 명세 확인: 요청할 URL, 메서드(GET, POST 등), 필요한 데이터를 알고 있어야 함.  

   ㅎㅇㅌ
