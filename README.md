# 이선우 포트폴리오

> LLM이 만든 결과를 코드로 검증하는 서비스를 만드는 백엔드 · AI 개발자입니다.
> 주요 문제 해결 사례는 <a href="https://sunwoolee.notion.site"><img src="https://img.shields.io/badge/-Notion_Portfolio-000000?style=for-the-badge&logo=notion&logoColor=white" height="20px" style="margin-bottom: -5px" /></a> 에 정리했습니다.

<br />

# Projects

캡스톤디자인 두 개와 개인 · 팀 프로젝트 세 개입니다.
팀 프로젝트는 제가 맡은 영역만 적었고, 개인 프로젝트는 기획부터 배포까지 혼자 했습니다.

## 1. 관계 메모리 에이전트

> 대화 속 호칭("팀장 → 김팀장 → 부장님")을 같은 사람으로 묶는 엔티티 해석과 평가 장치 _(캡스톤디자인 2 - 개인 프로젝트)_
>
> - 개발기간 : 2026.09 ~ 진행 중
> - 만든 것 : 대화에서 인물과 사건을 찾아 기존 인물과 연결하고, 확신이 부족하면 자동으로 합치지 않고 사용자에게 되묻는 파이프라인입니다. 모든 판정의 근거를 남겨 성능 지표를 원본 파일 하나로 다시 계산할 수 있습니다.
> - 해결한 것 : 첫 평가에서 제안 방식이 임베딩만 쓰는 단순한 방식보다 낮게 나왔습니다. 통과 기준을 바꾸지 않고 실패 케이스를 단계별로 추적해 확신도 계산과 규칙 필터를 고쳤고, F1 0.57에서 0.90이 됐습니다.
> - Language : Python
> - Skill : FastAPI, SQLAlchemy 2.0, Alembic, PostgreSQL + pgvector, OpenAI API, pytest, GitHub Actions, Docker
>
> [프로젝트 상세 설명](https://github.com/SunWoo1213/Relationship)

<br />

## 2. 에이전트 권한 브로커

> AI 에이전트의 도구 호출을 허용 · 거부 · 승인으로 판단하고 근거를 남기는 검문소 _(개인 프로젝트)_
>
> - 개발기간 : 2026.09 ~ 진행 중
> - 만든 것 : AI 에이전트가 사내 시스템을 호출할 때 반드시 거쳐 가는 중간 계층입니다. 에이전트는 실제 API 키를 갖지 않고, 모든 호출은 브로커가 정책으로 판단한 뒤 그 근거를 위변조가 드러나는 감사 로그로 남깁니다.
> - 해결한 것 : 통과하고 있던 정책 테스트 46개가 정작 출력 형식 계약을 검사하지 못하고 있었습니다. 정책을 한 줄씩 일부러 망가뜨려 실패해야 할 테스트가 정확히 실패하는지 확인하는 절차를 세워 찾아냈습니다.
> - Language : Python, Rego
> - Skill : OPA, Docker Compose, PostgreSQL, Redis, pytest, GitHub Actions
>
> [프로젝트 상세 설명](https://github.com/SunWoo1213/broker-agent)

<br />

## 3. AI Invest

> LLM이 쓴 투자 리포트의 숫자를 수집 데이터와 대조해, 통과한 리포트만 저장하는 서비스 _(캡스톤디자인 1 - 2인 팀 프로젝트)_
>
> - 개발기간 : 2026.03 ~ 2026.06
> - 만든 것 : 흩어진 글로벌 시장 데이터를 모아 보여 주고, LLM이 쓴 투자 리포트를 저장하기 전에 리포트 속 숫자가 실제 수집 데이터에 있는지 코드로 확인합니다. 백엔드와 배포를 맡았고 프론트엔드는 팀원이 담당했습니다.
> - 해결한 것 : 배포한 뒤 리포트가 한 건도 저장되지 않았습니다. 로그에 무엇이 남고 무엇이 없는지를 기준으로 범위를 좁혀 스케줄러, 외부 API 장애, DB 타입 세 가지 원인을 차례로 찾아 고쳤습니다.
> - Language : Python
> - Skill : FastAPI, SQLAlchemy, Alembic, PostgreSQL, LangGraph, OpenAI API, APScheduler, pytest, GitHub Actions, Render
>
> [프로젝트 상세 설명](https://github.com/SunWoo1213/AI-Invest)

<br />

## 4. AI 모의 면접

> 채용 공고 분석 · 자기소개서 피드백 · 음성 모의 면접 서비스 _(개인 프로젝트)_
>
> - 개발기간 : 2025.09 ~ 2025.12
> - 만든 것 : 채용 공고를 한 번 분석해 저장하고, 그 결과를 자기소개서 피드백과 면접 질문에 다시 씁니다. 면접은 질문 음성과 답변 녹음, 음성 인식, 다음 질문 생성을 한 번의 요청 안에서 처리합니다.
> - 해결한 것 : 처음에는 피드백으로 점수를 줬는데 점수만으로는 무엇을 고쳐야 할지 알 수 없었습니다. 점수를 없애고 강점과 개선점, 모범 답안을 주는 구조로 바꾸면서 이미 저장된 데이터는 감싸서 그대로 읽히게 했습니다.
> - Language : TypeScript
> - Skill : Next.js 14, PostgreSQL, AWS S3, OpenAI GPT-4o · TTS · Whisper, Vercel
>
> [프로젝트 상세 설명](https://github.com/SunWoo1213/Mock_interview)

<br />

## 5. 특허 RAG

> 특허 검색과 IPC 분류 코드 생성을 하나의 질의로 처리하는 RAG _(DS학술제 모델링 경진대회 장려상 - 2인 팀 프로젝트)_
>
> - 개발기간 : 2024.09 ~ 2024.11
> - 만든 것 : 특허 3,006건을 벡터DB에 넣고, 기존 특허를 찾는 질문과 새 발명의 분류 코드를 만드는 질문을 하나의 함수로 처리합니다. 검색과 생성 로직을 맡았고 데이터 라벨링은 팀원이 담당했습니다.
> - 해결한 것 : Agent에 맡기니 같은 종류의 질문인데도 조회로 갈 때와 생성으로 갈 때가 달랐습니다. 경로를 LLM이 고르지 않고 코드가 나누도록 라우터 체인으로 바꿔 질문마다 같은 경로를 타게 했습니다.
> - Language : Python
> - Skill : LangChain, ChromaDB, OpenAI API, ko-sroberta-multitask, Google Colab
>
> [프로젝트 상세 설명](https://github.com/SunWoo1213/Patent_Classification)

<br />

# Education · Certificate

> - 강남대학교 소프트웨어전공 · 인공지능전공(복수전공), 2021.03 ~ 2027.02(졸업예정)
> - 정보처리기사(2026.06), SQLD(2026.03)
> - 2024.11 강남대학교 데이터사이언스전공 학술제 장려상

<br />

# Contact

> - 이메일 : leesunwoo1954@gmail.com
> - 노션 : https://sunwoolee.notion.site
> - 깃허브 : https://github.com/SunWoo1213
