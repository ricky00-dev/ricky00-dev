# Hi, I'm ricky00 👋

Backend Developer | 단국대학교 소프트웨어학과

💻 Spring Boot & FastAPI 기반 백엔드 개발에 집중하고 있습니다
🎯 인증 · 캐싱 · 비동기/실시간 처리 구조 설계에 관심이 많습니다
📜 SQLD · ADsP 자격 보유

---

## 🛠 Tech Stack

**Backend**

![Spring Boot](https://img.shields.io/badge/Spring%20Boot-6DB33F?style=flat-square&logo=springboot&logoColor=white)
![FastAPI](https://img.shields.io/badge/FastAPI-009688?style=flat-square&logo=fastapi&logoColor=white)
![Java](https://img.shields.io/badge/Java-007396?style=flat-square&logo=openjdk&logoColor=white)
![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white)

**Database & Infra**

![Redis](https://img.shields.io/badge/Redis-DC382D?style=flat-square&logo=redis&logoColor=white)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1?style=flat-square&logo=postgresql&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white)
![AWS S3](https://img.shields.io/badge/AWS%20S3-569A31?style=flat-square&logo=amazons3&logoColor=white)

**Realtime & Tools**

![WebSocket](https://img.shields.io/badge/WebSocket-010101?style=flat-square&logo=socketdotio&logoColor=white)
![Git](https://img.shields.io/badge/Git-F05032?style=flat-square&logo=git&logoColor=white)
![GitHub](https://img.shields.io/badge/GitHub-181717?style=flat-square&logo=github&logoColor=white)

---

## 🚀 Projects

### Trender — 트렌드 기반 위치 서비스
`2026 ~ 진행 중 (출시 준비 중)` · **Backend 단독 담당** · FastAPI

SNS·AI로 장소를 발견하고 동선을 기록·공유하는 위치 기반 서비스. 모노레포 내 backend 스택을 단독 담당.

- **음성 리뷰** — 수십 초 걸리는 AI 처리를 비동기(`202` 즉시 응답 + 백그라운드)로 전환, 체감 대기시간 **최대 35초 → 1초 미만**. 완료 통지는 기존 WebSocket(Redis Pub/Sub)에 이벤트만 추가해 재사용
- **SNS2Map** — 2단계 Redis 캐싱으로 카카오 API 응답 **105ms → 캐시 0.17ms(약 600배)**, 동일 요청 반복 시 외부 호출 100% 제거
- **성능** — 동선 상세 조회에 복합 인덱스 적용, 15만 건 규모 실측(EXPLAIN ANALYZE)에서 **3.257ms → 0.052ms(약 62배)**
- **안정성** — 다중 워커 환경 멱등성 보장 리팩토링, 테스트 커버리지 64% → 90% (백엔드 테스트 315개 유지)

> 팀 프로젝트로 출시 준비 중이라 저장소는 비공개입니다. 상세 내용은 포트폴리오로 제공합니다.

### Union — 대학생 미니앱 슈퍼앱 플랫폼
`2024` · 팀 4명 · **Backend** · Spring Boot · 10개 도메인

퍼블리셔가 미니앱을 등록·배포하고 학생이 실행하는 슈퍼앱 플랫폼.

- 대시보드·백엔드가 공유하는 테이블의 **PK 충돌**(양쪽 INSERT, 신규 등록 실패)을 INSERT 통로 단일화로 해결
- 미들웨어 → 라우트 → 내부 JWT → `@PreAuthorize` → 멤버십의 **다단계 권한 가드**로 단일 우회 경로 차단
- 행동 이벤트 배치 수집·앱별 통계 집계, 식별자 SHA-256 해싱으로 개인정보 보호

---

## 📊 GitHub Stats

<!-- Stats 이미지가 안 뜨면 github-readme-stats 서버 일시 장애일 수 있습니다. 새로고침하거나, 계속 안 뜨면 이 섹션을 통째로 삭제해도 됩니다. -->

![ricky00-dev's GitHub stats](https://github-readme-stats.vercel.app/api?username=ricky00-dev&show_icons=true&hide_border=true&cache_seconds=1800)

![Top Langs](https://github-readme-stats.vercel.app/api/top-langs/?username=ricky00-dev&layout=compact&hide_border=true&cache_seconds=1800)
