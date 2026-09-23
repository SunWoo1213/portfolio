# 📜 이선우 포트폴리오

> 이선우(Sunwoo Lee) - SunWoo1213 포트폴리오

<br />

# 👋 Intro

> 안녕하세요! LLM이 만든 결과를 ***코드로 검증하는 서비스***를 만드는 백엔드 · AI 개발자 이선우입니다.   
> 문제를 어떻게 발견하고 해결했는지는 <a href="https://sunwoolee.notion.site"><img src="https://img.shields.io/badge/-Notion_Portfolio-000000?style=for-the-badge&logo=notion&logoColor=white" height="20px" style="margin-bottom: -5px" /></a> 에 자세히 정리했습니다.

<br />

# 📝 Projects

캡스톤디자인 두 개와 개인 · 팀 프로젝트 세 개입니다.  
팀 프로젝트는 제가 맡은 영역(백엔드 · 배포, 팀장으로 맡은 데이터 · 학습 · 통합, 검색 · 생성 로직)만 적었고, 개인 프로젝트는 기획부터 구현까지 혼자 했습니다.

## 1. 🧠 관계 메모리 에이전트

> 대화 속 호칭("팀장 → 김팀장 → 부장님")을 같은 사람으로 묶는 엔티티 해석과 평가 장치 _(캡스톤디자인 2 - 개인 프로젝트)_
>
> - 개발기간 : 2026.09 ~ 진행 중
> - 핵심 역할 : 전체 — 스키마 · 툴 7종 · 엔티티 해석 4단계 · 평가 장치(비교 방식 5종, 시나리오 40건)
> - 해결한 문제 : 파일럿 평가에서 임베딩 단독 방식에 밀린 원인 2개를 찾아 고치고 1회 재실행 → 40건 기준 오병합 0 · 미검출 0(채점 132 mention), F1 0.566 → 0.897
> - Language : Python
> - Skill : FastAPI, SQLAlchemy 2.0, Alembic, PostgreSQL + pgvector, OpenAI API, pytest, GitHub Actions, Docker
>
> [프로젝트 상세 설명](https://github.com/SunWoo1213/Relationship)

<br />

## 2. 📈 AI Invest

> LLM이 쓴 투자 리포트의 숫자를 수집 데이터와 대조해, 통과한 리포트만 저장하는 서비스 _(캡스톤디자인 1 - 2인 팀 프로젝트)_
>
> - 개발기간 : 2026.03 ~ 2026.06
> - 핵심 역할 : 백엔드 · 배포 — FastAPI API 41개 · 테이블 14개, LangGraph 리포트 파이프라인과 검증 게이트, 스케줄러, Render · Supabase 배포 (프론트엔드는 팀원)
> - 해결한 문제 : writer가 근거 없는 숫자를 쓰고 게이트가 부호만 다른 숫자까지 거부해 재작성 한도를 넘기며 NVDA 리포트가 저장되지 않던 문제를, 허용 숫자 목록 주입과 절댓값 비교로 게이트 기준은 유지한 채 해결
> - Language : Python
> - Skill : FastAPI, SQLAlchemy, Alembic, PostgreSQL, LangGraph, OpenAI API, APScheduler, pytest, GitHub Actions, Render
>
> [프로젝트 상세 설명](https://github.com/SunWoo1213/AI-Invest)

<br />

## 3. 🚗 차량 외관 부품 탐지 · 차종 분류

> 차량 사진 한 장에서 외관 부품 14종의 위치와 차종 100종을 함께 판별하는 비전 파이프라인 _(컴퓨터비전 기말과제 - 3인 팀 프로젝트, 팀장)_
>
> - 개발기간 : 2025.11 ~ 2025.12
> - 핵심 역할 : 팀장 — 데이터 전처리(라벨 COCO 변환, 연식을 차종으로 합친 100종 구성), YOLOX 학습 환경 구축 · 학습, ResNet50 차종 분류, 통합 추론 (백본 비교 · Hard Sample 추가 학습은 팀원)
> - 해결한 문제 : Windows에서 YOLOX 학습이 검증 단계마다 멈추던 문제를 학습 로그의 오류(이미지 폴더 경로 · `info` 키 · 평가 모듈 빌드 · 체크포인트 로드)를 순서대로 고쳐 해결하고, RTX 4070 SUPER에 맞춰 배치 24로 20 epoch 학습 → 검증 AP50 0.969 · AP50:95 0.836
> - Language : Python
> - Skill : PyTorch, YOLOX, torchvision(ResNet50), pycocotools, OpenCV, CUDA
>
> [프로젝트 상세 설명](https://github.com/SunWoo1213/Vehicle_CNN)

<br />

## 4. 🎤 AI 모의 면접

> 채용 공고 분석 · 자기소개서 피드백 · 음성 모의 면접 서비스 _(개인 프로젝트)_
>
> - 개발기간 : 2025.09 ~ 2025.12
> - 핵심 역할 : 전체 — 기획, 화면, API Routes 20개, PostgreSQL 테이블 7개, S3 · Vercel 배포
> - 해결한 문제 : 누구에게나 비슷한 질문이 나오던 면접을, 매 턴 공고 분석 · 자기소개서 · 대화 이력을 넣도록 바꿔 지원자에게 맞춘 질문으로 개선
> - Language : TypeScript
> - Skill : Next.js 14, PostgreSQL, AWS S3, OpenAI GPT-4o · TTS · Whisper, Vercel
>
> [프로젝트 상세 설명](https://github.com/SunWoo1213/Mock_interview)

<br />

## 5. 📑 특허 RAG

> 특허 검색과 IPC 분류 코드 생성을 하나의 질의로 처리하는 RAG _(DS학술제 모델링 경진대회 장려상 - 2인 팀 프로젝트)_
>
> - 개발기간 : 2024.09 ~ 2024.11
> - 핵심 역할 : 검색 · 생성 로직 — Retriever 3종, Self-Query 메타데이터 설계, LLM 라우터 체인 (데이터 라벨링 · 파악은 팀원)
> - 해결한 문제 : IPC 코드처럼 정확히 일치해야 하는 값을 임베딩 유사도로 찾기 어려워, 메타데이터 필터 문제로 바꿔 Self-Query Retriever 채택
> - Language : Python
> - Skill : LangChain, ChromaDB, OpenAI API, ko-sroberta-multitask, Google Colab
>
> [프로젝트 상세 설명](https://github.com/SunWoo1213/Patent_Classification)

<br />

# 🎓 Education · Certificate

> - 강남대학교 소프트웨어전공 · 인공지능전공(복수전공), 2021.03 ~ 2027.02(졸업예정)
> - 정보처리기사(2026.06), SQLD(2026.03)
> - 2024.11 강남대학교 데이터사이언스전공 학술제 장려상

<br />

# 📞 Contact

> - 이메일 : leesunwoo1954@gmail.com
> - 노션 : https://sunwoolee.notion.site
> - 깃허브 : https://github.com/SunWoo1213
