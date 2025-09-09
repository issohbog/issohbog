<!-- 기존 헤더 부분 그대로 유지 -->

![header](https://capsule-render.vercel.app/api?&type=waving&color=timeAuto&height=180&section=header&text=DoHyeon's%20Hub&fontSize=50&animation=fadeIn&fontAlignY=45)

<br>
<div align='center'>💻 깊고 넓게 공부하는 개발자 박도현(●'◡'●)입니다.</div>
<br>
<div align='center'> ✉ Email : <a href="mailto:qkrehgus2312@naver.com">qkrehgus2312@naver.com</a></div>
<div align='center'> 🔗 Notion : <a href="https://www.notion.so/25e09bf8c3c480e5b274e3a800193c3a?source=copy_link">노션 포트폴리오</a></div>
<br>
<br>
<br>

![Anurag's GitHub stats](https://github-readme-stats.vercel.app/api?username=issohbog&show_icons=true&theme=radical)  
![Top Langs](https://github-readme-stats.vercel.app/api/top-langs/?username=issohbog&layout=compact)

---

## 📌 Projects

### 🖥 MagicPOS — MVC 버전 (SpringBoot MVC + Thymeleaf)
- **Stack**  
  <img src="https://img.shields.io/badge/Spring_Boot-6DB33F.svg?style=flat-square&logo=Spring%20Boot&logoColor=white"/>&nbsp;
  <img src="https://img.shields.io/badge/Thymeleaf-005F0F.svg?style=flat-square&logo=Thymeleaf&logoColor=white"/>&nbsp;
  <img src="https://img.shields.io/badge/MyBatis-000000.svg?style=flat-square&logoColor=white"/>&nbsp;
  <img src="https://img.shields.io/badge/MySQL-4479A1.svg?style=flat-square&logo=MySQL&logoColor=white"/>&nbsp;
  <img src="https://img.shields.io/badge/Spring%20Security-6DB33F.svg?style=flat-square&logo=Spring%20Security&logoColor=white"/>&nbsp;

- **Overview**: 좌석 예약, 요금제/상품 관리, 회원 관리, 결제/로그 분석까지 하나의 서버(MVC)에서 처리하는 통합 관리 시스템  

- **My Role**  

  #### 🏪 매장 관리
  - **좌석 예약 및 종료**: 로그인 시 `user_tickets`에서 남은 시간을 조회 후 좌석 예약, 로그아웃 시 사용 시간만큼 FIFO 방식으로 차감  
  - **좌석 상태 관리**:  
    - 사용 중 좌석 → 남은 시간이 60분 이상이면 **녹색**, 60분 이하이면 **빨간색** 표시  
    - 고장 좌석은 **노란색**, 로그아웃 시에는 **휴지통 아이콘** 표시 → 관리자가 클릭 시 이용 가능 좌석으로 변경  
  - **실시간 반영**: WebSocket을 이용해 좌석 상태 변화를 알림 및 대시보드에 즉시 반영  

  #### 🎫 요금제 구매 (관리자/사용자)
  - **관리자 구매**:  
    - 관리자 화면에서 회원 검색 → 해당 회원에게 현금/카드 결제 기반 요금제 구매 가능  
    - JS 이벤트로 키 입력 감지 후 실시간 회원 검색 리스트 제공  
  - **TossPayments 결제 연동**:  
    - 신용카드 결제 시 TossPayments 모듈 호출  
    - 결제 성공 후 `user_tickets` 테이블에 구매 내역 저장 (관리자/사용자 공통) 

  #### 🧑🏻 회원 관리
  - **CRUD**: 회원 등록·수정·삭제(일괄 삭제), 조회 기능 구현  
  - **ID 중복 체크**: 등록 시 Ajax 비동기 통신으로 실시간 중복 확인  
  - **비밀번호 초기화**: 회원 정보 화면에서 비밀번호 초기화 → 암호화 후 UPDATE  
  - **페이지네이션**: 대량 데이터에서도 빠른 조회 가능하도록 구현  

  #### 📦 상품 관리
  - **상품 분류/상품 CRUD**: 관리자가 상품과 상품 분류를 등록·수정·삭제 가능  
  - **파일 업로드**: 상품 이미지 업로드 및 수정 기능 구현  
  - **페이지네이션**: 대량 상품 목록 관리 최적화  

  #### 👤 회원 가입
  - **유효성 검사**: 입력 값에 대해 실시간 검사 및 경고 문구 표시 → 올바른 데이터만 저장  

👉 [프로젝트 Repo](https://github.com/issohbog/PowerManager_ReactREST)

---

### 🖥 MagicPOS — Client/Server 분리 버전 (SpringBoot RestAPI + React) 
- **Stack**  
  <img src="https://img.shields.io/badge/React-61DAFB.svg?style=flat-square&logo=React&logoColor=black"/>&nbsp;
  <img src="https://img.shields.io/badge/Tailwind_CSS-06B6D4.svg?style=flat-square&logo=tailwindcss&logoColor=white"/>&nbsp;
  <img src="https://img.shields.io/badge/Spring_Boot-6DB33F.svg?style=flat-square&logo=Spring%20Boot&logoColor=white"/>&nbsp;
  <img src="https://img.shields.io/badge/REST%20API-000000.svg?style=flat-square&logoColor=white"/>&nbsp;
  <img src="https://img.shields.io/badge/JWT-000000.svg?style=flat-square&logo=JSON%20Web%20Tokens&logoColor=white"/>&nbsp;
  <img src="https://img.shields.io/badge/MyBatis-000000.svg?style=flat-square&logoColor=white"/>&nbsp;
  <img src="https://img.shields.io/badge/MySQL-4479A1.svg?style=flat-square&logo=MySQL&logoColor=white"/>&nbsp;
  <img src="https://img.shields.io/badge/WebSocket-4285F4.svg?style=flat-square&logoColor=white"/>&nbsp;
- **Overview**: 프론트(React)와 백엔드(Spring Boot REST) 분리, 
- **My Role**  
  - REST API 설계(인증/권한, 좌석/요금제, 주문/정산) 및 예외/검증 규약 수립  
  - Spring Security + JWT 무상태 인증, CORS/필터 체인 구성  
  - React 좌석 관리 UI, 드래그/매핑, 실시간(WebSocket) 좌석 상태 업데이트  
  - 비동기 상태 관리, API 에러/로딩 UX, 페이징/검색/필터 도입  
👉 Front Repo: `https://github.com/username/magicpos-react`  
👉 Back Repo: `https://github.com/username/magicpos-rest`  (수정해서 사용)

<details>
  <summary>아키텍처/API 문서 & 더보기</summary>

  - Client: React + Tailwind, 상태 관리/라우팅 구조
  - Server: Spring Boot, 도메인 계층, 보안 필터/핸들러 구성
  - (Swagger/포스트맨, 시연 영상 링크 삽입 위치)
</details>

---

### 🛒 NeoBel (화장품 쇼핑몰, JSP/Servlet)
- **Stack**  
  <img src="https://img.shields.io/badge/JSP-FFA000.svg?style=flat-square&logoColor=white"/>&nbsp;
  <img src="https://img.shields.io/badge/Servlet-6DB33F.svg?style=flat-square&logoColor=white"/>&nbsp;
  <img src="https://img.shields.io/badge/MyBatis-000000.svg?style=flat-square&logoColor=white"/>&nbsp;
  <img src="https://img.shields.io/badge/MySQL-4479A1.svg?style=flat-square&logo=MySQL&logoColor=white"/>&nbsp;
- **Overview**: 장바구니/주문/결제 흐름까지 포함한 쇼핑몰 핵심 기능 구현
- **My Role**  
  - 상품/주문 CRUD, 세션 장바구니 → 주문 테이블 적재 흐름 구현  
  - Repository/Service/Controller 구조 정리, 예외/검증 처리  
👉 Repo: `https://github.com/username/neobel`

---

### 🚌 공항버스 조회 시스템 (OpenAPI)
- **Stack**  
  <img src="https://img.shields.io/badge/Java-007396.svg?style=flat-square&logo=OpenJDK&logoColor=white"/>&nbsp;
  <img src="https://img.shields.io/badge/JSP-FFA000.svg?style=flat-square&logoColor=white"/>&nbsp;
  <img src="https://img.shields.io/badge/MyBatis-000000.svg?style=flat-square&logoColor=white"/>&nbsp;
  <img src="https://img.shields.io/badge/MySQL-4479A1.svg?style=flat-square&logo=MySQL&logoColor=white"/>&nbsp;
  <img src="https://img.shields.io/badge/OpenAPI-02569B.svg?style=flat-square&logo=Swagger&logoColor=white"/>&nbsp;
- **Overview**: 공공데이터 API 수집/적재, 조건 검색(출발/도착/시간대) 제공
- **My Role**  
  - API 수집 자동화 스케줄링, 파싱/정제 후 DB 적재  
  - 조건 검색 쿼리 최적화 및 페이징/정렬 구현  
👉 Repo: `https://github.com/username/bus-api-project`

---

<h3 align="center">📚 Tech Stack 📚</h3>
<div align="center">

  <!-- Languages -->
  <img src="https://img.shields.io/badge/Java-007396.svg?style=flat-square&logo=OpenJDK&logoColor=white"/>&nbsp;
  <img src="https://img.shields.io/badge/JavaScript-F7DF1E.svg?style=flat-square&logo=JavaScript&logoColor=black"/>&nbsp;
  <img src="https://img.shields.io/badge/Python-3776AB.svg?style=flat-square&logo=Python&logoColor=white"/>&nbsp;
  <img src="https://img.shields.io/badge/C-A8B9CC.svg?style=flat-square&logo=C&logoColor=white"/>&nbsp;
  <img src="https://img.shields.io/badge/C++-00599C.svg?style=flat-square&logo=C%2B%2B&logoColor=white"/>&nbsp;
  <br/>

  <!-- Backend & Frameworks -->
  <img src="https://img.shields.io/badge/Spring_Framework-6DB33F.svg?style=flat-square&logo=Spring&logoColor=white"/>&nbsp;
  <img src="https://img.shields.io/badge/Spring_Boot-6DB33F.svg?style=flat-square&logo=Spring%20Boot&logoColor=white"/>&nbsp;
  <img src="https://img.shields.io/badge/MyBatis-000000.svg?style=flat-square&logoColor=white"/>&nbsp;
  <img src="https://img.shields.io/badge/Apache%20Tomcat-F8DC75?style=flat-square&logo=Apache%20Tomcat&logoColor=black"/>&nbsp;
  <br/>

  <!-- Database & Tools -->
  <img src="https://img.shields.io/badge/MySQL-4479A1.svg?style=flat-square&logo=MySQL&logoColor=white"/>&nbsp;
  <img src="https://img.shields.io/badge/DBMS-003B57.svg?style=flat-square&logoColor=white"/>&nbsp;
  <img src="https://img.shields.io/badge/Git-F05032.svg?style=flat-square&logo=Git&logoColor=white"/>&nbsp;
  <img src="https://img.shields.io/badge/GitHub-181717.svg?style=flat-square&logo=GitHub&logoColor=white"/>&nbsp;
  <img src="https://img.shields.io/badge/VSCode-007ACC.svg?style=flat-square&logo=Visual%20Studio%20Code&logoColor=white"/>&nbsp;
  <img src="https://img.shields.io/badge/Eclipse-2C2255.svg?style=flat-square&logo=Eclipse%20IDE&logoColor=white"/>&nbsp;
  <img src="https://img.shields.io/badge/Django-092E20.svg?style=flat-square&logo=django&logoColor=white"/>&nbsp;
  <img src="https://img.shields.io/badge/Flutter-02569B.svg?style=flat-square&logo=flutter&logoColor=white"/>&nbsp;
  <br/>

  <!-- Frontend -->
  <img src="https://img.shields.io/badge/HTML5-E34F26.svg?style=flat-square&logo=HTML5&logoColor=white"/>&nbsp;
  <img src="https://img.shields.io/badge/CSS3-1572B6.svg?style=flat-square&logo=CSS3&logoColor=white"/>&nbsp;
  <img src="https://img.shields.io/badge/Tailwind_CSS-06B6D4.svg?style=flat-square&logo=tailwindcss&logoColor=white"/>&nbsp;
  <img src="https://img.shields.io/badge/Bootstrap-7952B3.svg?style=flat-square&logo=Bootstrap&logoColor=white"/>&nbsp;
  <img src="https://img.shields.io/badge/React-61DAFB.svg?style=flat-square&logo=React&logoColor=black"/>&nbsp;
  <img src="https://img.shields.io/badge/jQuery-0769AD.svg?style=flat-square&logo=jQuery&logoColor=white"/>&nbsp;
  <img src="https://img.shields.io/badge/JSP-FFA000.svg?style=flat-square&logoColor=white"/>&nbsp;
  <img src="https://img.shields.io/badge/Ajax-4285F4.svg?style=flat-square&logoColor=white"/>&nbsp;

</div>

![footer](https://capsule-render.vercel.app/api?type=waving&color=auto&height=100&section=footer)
