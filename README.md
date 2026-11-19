<div align="center">
<img width="200" height="265" alt="양준호 증명사진" src="https://github.com/user-attachments/assets/4e6e3d34-fa58-43f3-9f9e-67384132fd42" />

## 서비스의 동작을 이해하고, 문제의 원인을 찾아가는 Backend Developer, 양준호입니다.

#### 단국대학교 컴퓨터공학과 · 카카오임팩트 테크포임팩트리빙랩 1기 · 멋쟁이사자처럼 14기

Spring Boot나 FastAPI 같은 프레임워크 기반의 백엔드를 개발하며, <br/>
실시간 통신과 데이터 저장, 클라우드 환경까지 경험을 넓혀가고 있습니다.

<br/>

![GPA 4.13 / 4.5](https://img.shields.io/badge/GPA-4.13%20%2F%204.5-2766EC?style=for-the-badge&labelColor=555555)
![NCA 취득](https://img.shields.io/badge/NCA-%EC%B7%A8%EB%93%9D-087F36?style=for-the-badge&labelColor=555555)
![Deployment Naver Cloud, AWS, Cloudflare Pages](https://img.shields.io/badge/Deployment-Naver%20Cloud%20%C2%B7%20AWS%20%C2%B7%20Cloudflare%20Pages-F38020?style=for-the-badge&labelColor=555555)

[![GitHub](https://img.shields.io/badge/GitHub-Novice--Dev--Robin-181717?style=for-the-badge&logo=github&logoColor=white)](https://github.com/Novice-Dev-Robin)
[![Email](https://img.shields.io/badge/Email-Dev.Robin03%40gmail.com-EA4335?style=for-the-badge&logo=gmail&logoColor=white)](mailto:Dev.Robin03@gmail.com)

</div>

---

## About Me

처음 나만의 갤러리를 
기능을 구현하는 과정에서 **요청이 어떤 경로를 거쳐 처리되고, 데이터가 어디에 저장되는지** 이해하는 데 관심이 있습니다.

졸업 작품 **tikitaka**의 프론트엔드, 백엔드 개발에 참여하며 기획부터 디자인, DB 설계 및 API 설계, 서버 배포 경험이 있습니다.
배포 과정에서 발생한 통신 문제를 브라우저·프록시·애플리케이션 구간으로 나누어 살펴보고, 동시 필기 환경에서 드러난 저장 대기 문제를 팀과 함께 개선했습니다.

저는 개발하면서 다음을 중요하게 생각합니다.

- **흐름 이해** — API 하나를 넘어 클라이언트, 서버, 데이터베이스가 연결되는 과정을 확인합니다.
- **원인 분석** — 주소·포트·프로토콜·처리 구간을 나누어 문제가 발생한 지점을 찾습니다.
- **사용자 경험에서의 관점** — 동작 여부와 함께 실제 사용자가 느끼는 지연과 불편을 살펴봅니다.

---

## Projects

### 1. 📝 tikitaka — 실시간 강의 필기 공유 및 AI 기반 질문 아카이빙 플랫폼 

**2026 캡스톤디자인 · 4인 팀 · Backend**

![Award](https://img.shields.io/badge/2026%20단국%20G--RISE%20컨소시엄%20캡스톤디자인%20경진대회-장려상-D4A72C?style=flat-square)
![Role](https://img.shields.io/badge/Role-Backend-2766EC?style=flat-square)

강의자료 위에 교수자의 공유 필기, 학생의 개인 필기, 위치 기반 질문과 답변을 연결하는 학습 플랫폼입니다. 강의 중의 소통을 기록으로 남겨 강의 이후에도 복습할 수 있도록 만들었습니다.

**프로젝트에서 다룬 문제**

- **실시간 공유와 저장** — 교수자의 필기를 학생 화면에 전달하고, 슬라이드별 필기 기록을 다시 조회하는 흐름을 다뤘습니다.
- **학습 기록의 연결** — 강의자료·슬라이드·질문·답변을 연결하는 데이터 모델과 API를 설계했습니다.
- **인증과 접근 제어** — JWT 인증과 강의 참여자·역할에 따른 접근 권한을 다뤘습니다.
- **배포와 통신** — Cloudflare와 EC2를 연결하는 과정에서 HTTP/HTTPS 및 WebSocket 요청 경로를 확인했습니다.
- **알게 된 지식에 대한 기록** - 위에서 다룬 문제들을 통틀어, 전체 시스템 흐름을 읽고, 시스템 아키텍처로 도식화하였습니다.

<details>
<summary><strong>운영 검증과 확장 설계</strong></summary>

<br/>

| 구분 | 경험 |
| --- | --- |
| 테스트 환경 | EC2 t3.micro에서 Spring Boot·Nginx·Python AI 프로세스 운영 |
| 동시 동작 검증 | 공유 필기 수신자 30명과 개인 필기 작성자 20명 조건에서 수신·저장 정합성 확인 |
| 발견한 문제 | 빠른 필기 입력 시 저장 대기 누적 |
| 팀의 개선 | 프론트엔드 적응형 묶음 전송 적용 |
| 후속 분석 | DB 연결 점유와 요청 처리 시간 프로파일링 |
| 확장 설계 | ALB·다중 Spring Boot 서버·RabbitMQ 외부 브로커·AI 자원 분리 검토 |

</details>
<br/>
<table>
  <tr>
    <th width="50%">현재 시스템 아키텍처</th>
    <th width="50%">확장 이후 시스템 아키텍처</th>
  </tr>
  <tr>
    <td align="center">
      <img width="100%" alt="현재 시스템 아키텍처"
        src="https://github.com/user-attachments/assets/55d8cc22-cb78-4a81-aa3c-1cf6c43b1fd1" />
    </td>
    <td align="center">
      <img width="100%" alt="확장 시스템 아키텍처"
        src="https://github.com/user-attachments/assets/820d528a-8b2a-46d6-bba9-9a1b4d370cba" />
    </td>
  </tr>
</table>

<br/>

![Java](https://img.shields.io/badge/Java-007396?style=flat-square&logo=openjdk&logoColor=white)
![Spring Boot](https://img.shields.io/badge/Spring_Boot-6DB33F?style=flat-square&logo=springboot&logoColor=white)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1?style=flat-square&logo=postgresql&logoColor=white)
![WebSocket](https://img.shields.io/badge/WebSocket-010101?style=flat-square)
![AWS](https://img.shields.io/badge/AWS_EC2-FF9900?style=flat-square&logo=amazonec2&logoColor=white)

<!-- TikiTaka 저장소·시연 영상·서비스 링크와 직접 담당한 API 범위를 추가하면 프로젝트 기여를 더 명확히 보여줄 수 있습니다. -->
<!-- 화면 추가 예시: ![TikiTaka 강의 노트](assets/tikitaka-note.png) -->

---

### 2. ☁️ NAVER Cloud Platform — 웹 서비스 인프라 구성

**2026 구름타조정산소 - Clova OCR API를 활용한 온라인 정산 플랫폼**

네이버클라우드 플랫폼에서 **Web·API·DB로 역할을 나눈 서비스 구조**를 다루며, 외부 요청이 서버를 거쳐 데이터베이스에 도달하는 경로와 각 구간의 접근 제어를 학습했습니다.

- **서버 역할 분리** — Web·API·DB의 책임과 서버 사이의 요청 흐름을 정리했습니다.
- **네트워크 구조** — VPC·Subnet·Internet Gateway의 역할과 Public Subnet의 외부 통신 경로를 학습했습니다.
- **로드밸런서와 접근 제어** — ALB에서 Web 서버로 전달되는 요청을 기준으로 ACG 인바운드 규칙과 허용 대상을 검토했습니다.
- **DB 연결** — API 서버와 MySQL 서버 사이의 연결 방향, 포트 및 접근 허용 범위를 확인했습니다.
- **아키텍처 문서화** — 구성 요소와 통신 경로를 다이어그램으로 정리하고, 각 서버의 역할과 연결 이유를 설명했습니다.

<img width="1375" height="670" alt="구름타조정산소 시스템 아키텍처 제출본" src="https://github.com/user-attachments/assets/21b118b2-c288-47a6-8ef0-d723e5f07e72" />

| 관점 | 학습·검토 내용 |
| --- | --- |
| 요청 흐름 | 사용자 요청이 로드밸런서·Web·API·DB를 거치는 과정 |
| 네트워크 | Public Subnet과 Internet Gateway의 관계, 공인·사설 IP 구분 |
| 접근 제어 | 서버별 필요한 통신을 기준으로 한 ACG 인바운드·아웃바운드 규칙 |
| 구성 설명 | 서버를 나눈 이유와 각 연결 구간의 목적을 아키텍처로 표현 |

![NAVER Cloud](https://img.shields.io/badge/NAVER_Cloud_Platform-03C75A?style=flat-square)
![VPC](https://img.shields.io/badge/VPC-2766EC?style=flat-square)
![ALB](https://img.shields.io/badge/Application_Load_Balancer-2766EC?style=flat-square)
![ACG](https://img.shields.io/badge/ACG-2766EC?style=flat-square)
![MySQL](https://img.shields.io/badge/MySQL-4479A1?style=flat-square&logo=mysql&logoColor=white)

<!-- 네이버클라우드 프로젝트의 저장소·발표자료·아키텍처 이미지 링크를 추가할 수 있습니다. -->

---

## Learning & Records

### 🦁 단국대학교 멋쟁이사자처럼 14기 백엔드 스터디

Java 기본기에서 HTTP와 Spring Boot로 이어지는 학습 내용을 기록하고 있습니다.

- 타입 캐스팅, 문자열, List·Map 등 Java 기초
- 객체지향과 예외 처리, 회원가입 프로그램 실습
- HTTP·쿠키·세션, MVC 및 기본 CRUD 학습

[Backend Study](https://octagonal-chicory-02a.notion.site/3217a057c00180e38d2ffa25aa81e9dd?pvs=74)

---

## Tech Stack

### Backend & Data

![Java](https://img.shields.io/badge/Java-007396?style=for-the-badge&logo=openjdk&logoColor=white)
![Spring Boot](https://img.shields.io/badge/Spring_Boot-6DB33F?style=for-the-badge&logo=springboot&logoColor=white)
![JPA](https://img.shields.io/badge/Spring_Data_JPA-6DB33F?style=for-the-badge&logo=spring&logoColor=white)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1?style=for-the-badge&logo=postgresql&logoColor=white)

### Deployment & Tools

![NAVER Cloud](https://img.shields.io/badge/NAVER_Cloud_Platform-03C75A?style=for-the-badge)
![EC2](https://img.shields.io/badge/AWS_EC2-FF9900?style=for-the-badge&logo=amazonec2&logoColor=white)
![Nginx](https://img.shields.io/badge/Nginx-009639?style=for-the-badge&logo=nginx&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=for-the-badge&logo=docker&logoColor=white)
![GitHub Actions](https://img.shields.io/badge/GitHub_Actions-2088FF?style=for-the-badge&logo=githubactions&logoColor=white)
![Git](https://img.shields.io/badge/Git-F05032?style=for-the-badge&logo=git&logoColor=white)

### Also Experienced

![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=flat-square&logo=javascript&logoColor=black)
![React](https://img.shields.io/badge/React-20232A?style=flat-square&logo=react&logoColor=61DAFB)
![Vite](https://img.shields.io/badge/Vite-646CFF?style=flat-square&logo=vite&logoColor=white)
![Firebase](https://img.shields.io/badge/Firebase-DD2C00?style=flat-square&logo=firebase&logoColor=white)
![Cloudflare Pages](https://img.shields.io/badge/Cloudflare_Pages-F38020?style=flat-square&logo=cloudflarepages&logoColor=white)

## Experience

### 국가근로 : (주)나비온 · 웹 개발
**2025.09.01 ~ 2026.02.13**

- 회사 웹사이트: https://spacecasting.co.kr
- 기존 `product` 테이블을 백업한 뒤 규격별 단위 가격을 `price` 테이블로 분리하는 DB 정규화 작업 수행
- 변경된 DB 구조에 맞춰 Java·JSP 코드를 수정하고 기존 사이트 유지보수 수행

## Activities

### 멋쟁이사자처럼 14기 · 백엔드 운영진
**2026.03.03 ~ 2026.11.10**

- Java·Spring 기초, REST API, 서버 배포를 주제로 백엔드 스터디 운영
- 백엔드 파트 8명을 대상으로 1~2학기 스터디 진행
- 실습 과제 운영, 코드 리뷰 및 질의응답 진행

### 창업동아리 아두위두 · 교육 및 콘텐츠 제작
**2022.04.01 ~ 2023.01.20**

- 초·중·고등학생 대상 자체 개발 아두이노 키트 활용 교육 진행
- Arduino UNO를 활용한 LED 작동 실습 교육
- 클래스101 Fusion 360 강의자료 제작 보조 및 고등학생 대상 원데이클래스 운영
- 3D 프린팅·화산석을 활용한 천연 가습 무드등 ‘갓일’ 크라우드펀딩 참여
- 크라우드펀딩 모금액 **937,600원**

## Awards

| 수상일 | 대회 | 수상 | 프로젝트 |
| --- | --- | --- | --- |
| 2026.06.24 | 2026 단국 G-RISE사업단 컨소시엄 캡스톤디자인 경진대회 | 장려상 | **tikitaka** · 실시간 강의 필기 공유 및 AI 기반 질문 아카이빙 플랫폼 |
| 2025.12.22 ~ 2025.12.23 | 춘천시 및 SDU 데이터보안활용 혁신융합대학 사업단 주관 2025 기업데이터활용 AI 경진대회 | 우수상 | **떴냐?떴다!** - 푸드트럭 사장님들을 위한 홍보용 플랫폼 |

## Military

- **대한민국 육군 병장 만기전역** · 2023.02.20 ~ 2024.08.19

## Contact

- **전화번호**: 010-8832-1401
- **이메일**: [dev.robin03@gmail.com](mailto:dev.robin03@gmail.com)
