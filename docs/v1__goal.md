# 기능
- 로그인 기능 - 자체 로그인과 google oauth를 지원할것
- 본인이 작성한 모든 메모를 볼 수 있을 것
- 파일과 이미지 등도 볼 수 있을 것
- Chatgpt가 요약, 태깅 등을 해줄 것
- 검색할 때, 본인이 작성한 키워드, chatgpt 요약, 태깅을 검색할 수 있을 것


# 인프라
- 내 개인서버에 개발용이 자동 배포 될 것
- 최소한의 운영비
- 운영은 AWS 고려


```mermaid
---
title: Architecture
---
flowchart
  User
  Scheduler

  User -->|create_content| APIServer([APIServer])
  APIServer --> DB([DB-PostgreSQL])
  DB <--> Scheduler
  Scheduler --> ChatGPT
```