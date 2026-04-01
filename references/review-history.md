# 네이밍 검토 이력

> **관리 원칙**: SharePoint 최신 발행 문서 기준으로 유지. 버전 업데이트 시 이 파일도 동기화할 것.

---

## AAEF — Test 사업부 (최신: v2, 2026-03-31)

**솔루션명 (가칭)**: AAEF (AI Agent Evaluation Framework)
**핵심 기능**: AI 에이전트 신뢰성·성능 자동 평가 프레임워크
**⚠️ 가칭 충돌 주의**: RagaAI가 'AAEF(Agentic Application Evaluation Framework)'를 공식 브랜드로 사용 중 → 외부 표기·마케팅에 가칭 AAEF 사용 금지

**네이밍 후보 검토 결과**:

| 후보명 | 최종 AIWORKX 브랜드명 | 결과 | 비고 |
|--------|----------------------|------|------|
| AgentProbe | AIWORKX AgentProbe | ✅ **1순위** | 상표권 안전, NRB 방법론 직결, 경쟁사 충돌 없음 |
| EvalProbe | AIWORKX EvalProbe | ✅ **2순위 (v2 신규)** | Eval+Probe 조합, 기술적 정확성 우수 |
| ReliProbe | AIWORKX ReliProbe | ✅ **3순위 (v2 신규)** | Reliability 차별점 명확 |
| TrustBench | AIWORKX TrustBench | — 유지 | AI 신뢰성 직접 반영, Bench 시리즈 일관성 |
| AgentAudit | — | ❌ 탈락 | 미국 상표 충돌 위험 |
| AgentGuard | — | ❌ 탈락 | 주요 경쟁사 다수 사용 중 |
| AgentBench | — | ❌ 탈락 | Tsinghua THUDM ICLR 2024 논문·GitHub 브랜드 충돌 |

**최종 추천**:
- 1순위: **AIWORKX AgentProbe** — 상표권·경쟁사 리스크 없음, NRB 방법론 직결
- 2순위: **AIWORKX EvalProbe** — Eval+Probe 조합 기술적 정확성 우수

**다음 단계**: 법무팀 AgentProbe·EvalProbe KIPRIS Class 42 정식 조회 → NRB 상정

**SharePoint**: [Test_AAEF_네이밍검토_20260331.docx](https://testworks.sharepoint.com/sites/aiworkx-/Shared%20Documents/네이밍%20검토/Test/AAEF_20260331/Test_AAEF_네이밍검토_20260331.docx)

---

## Q One — Test 사업부 (최신: v2, 2026-03-31)

**솔루션명 (가칭)**: Q One (AI 기반 Web/App UI 테스트 자동화 솔루션)
**핵심 기능**: 스텝 기반 + AI 의도 기반 UI 테스트 자동화, ToD/NLU 통합, 온프레미스 LLM, Persona 기반 테스트, 금융·공공 특화

**네이밍 후보 검토 결과**:

| 후보명 | 최종 AIWORKX 브랜드명 | 결과 | 비고 |
|--------|----------------------|------|------|
| UIProbe | AIWORKX UIProbe | ✅ **1순위** | 상표권 안전, Probe 토큰 기등재, NLU·Intent 직결 |
| IntentProbe | AIWORKX IntentProbe | ✅ **2순위 (v2 신규)** | Q One 핵심 차별점(NLU Intent) 직접 반영 |
| FlowProbe | AIWORKX FlowProbe | ✅ **3순위 (v2 신규)** | 흐름(Flow)+탐침(Probe), 직관적 |
| UXProbe | AIWORKX UXProbe | ⚠️ **4순위 (v2 신규)** | UI/UX 테스트 포지셔닝 명확, 글로벌 직관 — 아래 Concerns 참조 |
| AppBench | AIWORKX AppBench | 🔴 **보류** | appbench.ai(YC 기반) 충돌 — 법무팀 조회 완료 전까지 보류 |
| SceneScan | — | ❌ 탈락 | Nerian Vision·Wärtsilä 등록 상표 충돌 |

### UXProbe Concerns

| 항목 | 내용 |
|------|------|
| **포지셔닝 범위** | UX는 UI보다 넓은 개념 — 사용성·접근성·디자인 전반을 포함. Q One의 실제 기능(UI 자동화 테스트)보다 범위가 넓어 제품 기능 오버프로미스 위험 |
| **경쟁사 연상** | UX Testing 카테고리에서 UserTesting, Hotjar, Maze 등 UX 리서치 도구와 혼동 가능 — Q One은 기능 테스트 자동화이지 UX 리서치 툴이 아님 |
| **내부 일관성** | Probe 시리즈(UIProbe·AgentProbe·FarmProbe 등)에서 앞 토큰이 기술 기능을 지칭하는데, UX는 기술 스택이 아닌 사용자 경험 레이어 → 시리즈 일관성 저하 |
| **타겟 고객 오인** | 금융·공공 특화 제품에서 "UX"는 UI/디자인 부서 연상 강함 — 실제 타겟(QA팀·개발팀)과 괴리 |
| **결론** | UIProbe가 Q One의 실제 기능(UI 자동화)을 더 정확하게 표현. UXProbe는 포지셔닝 확장 시 고려 가능하나 현재 1순위 부적합 |

**최종 추천**:
- 1순위: **AIWORKX UIProbe** — 상표권 안전, Probe 기등재 토큰, 외부 표기 직관
- 2순위: **AIWORKX IntentProbe** — NLU Intent 핵심 차별점 직접 반영

**다음 단계**: NRB 상정 (UIProbe 1순위·IntentProbe 대안 병행), Brand Governance 레지스트리 업데이트

**SharePoint**: [Test_QOne_네이밍검토_20260331.docx](https://testworks.sharepoint.com/sites/aiworkx-/Shared%20Documents/네이밍%20검토/Test/QOne_20260331/Test_QOne_네이밍검토_20260331.docx)

---

## ToD™ — Technology Ingredient Brand (최신: v3 rev.3, 2026-03-31)

**검토 대상**: AIWORKX 기술 인그리디언트 브랜드 `ToD™` (Powered by ToD™ 표기용)
**현행 정의**: Task-oriented Deterministic AI

**검토 경과**:
| 회차 | 날짜 | 주요 내용 |
|------|------|----------|
| v1 | 2026-03-20 | Linea™·Axia™ 제안 → AX prefix 전략 전환 결정 |
| v2 | 2026-03-26 | AXO/AXON/AXEN 검토 → 상표·업종 충돌 탈락 |
| v3 | 2026-03-30 | AXDO™ 1순위 확정, AXDC™ 신규 추가 (4순위) |
| v3 rev.3 | 2026-03-31 | **AXDC™ 1순위 승격, AXDO™ 2순위로 조정** |

**v3 rev.3 후보 순위**:

| 순위 | 후보 | 발음 | 풀네임 | TM 리스크 |
|------|------|------|--------|----------|
| ★ 1순위 | **AXDC™** | /악-디씨/ | AX+DC (Direct Compute / AC→DC 메타포) | KIPRIS Class 42 조회 필요 |
| 2순위 | AXDO™ | /악-두/ | AX+DO (실행·완수) | 클린 |
| 3순위 | AXHIT™ | /악-힛/ | AX+HIT (목표 명중·달성) | 클린 |
| 4순위 | AXGO™ | /악-고/ | AX+GO (실행 개시) | 클린 |
| 5순위 | AXRUN™ | /악-런/ | AX+RUN (작동·실행) | 클린 |
| 6순위 | AXSET™ | /악-셋/ | AX+SET (완료·세팅) | 클린 |

**⚠️ AXDC™ 주의사항**: AC/DC 록밴드 연상 → 보수적 엔터프라이즈(금융·공공) 고객군 이미지 부담 가능. 글로벌 출원 전 법무팀 AC/DC 상표 혼동 가능성 사전 확인 필수.

**탈락 후보 누적 (v1~v3, 총 12개)**: AXO, AXON, AXEN, AXCO, AXFIN, AXEND, AXMIT, AXIM, AXIVE, AXEVO, AXELO, AXWORK

**최종 추천**:
- 1순위: **AXDC™** — AC/DC 변형, 이중 레이어 의미(기술적·전략적), 브랜드 임팩트 우위 (KIPRIS 확인 후 NRB 상정)
- 2순위: **AXDO™** — 실행·완수 직관적, 상표 클린, 즉시 출원 가능

**다음 단계**: 법무팀 AXDC™ KIPRIS Class 42 정식 조회 + AC/DC 상표 혼동 가능성 검토 → NRB 1순위 상정

**SharePoint**: [기타_ToD_네이밍검토_20260331_v3r3.docx](https://testworks.sharepoint.com/sites/aiworkx-/Shared%20Documents/네이밍%20검토/기타/ToD_20260330_v3/기타_ToD_네이밍검토_20260331_v3r3.docx)

---

## blackolive — Data 사업부 (최신: v3, 2026-03-31)

**솔루션명 (가칭)**: blackolive
**핵심 기능**: 비정형 데이터(문서·이미지·음성) AI 활용 가능 형태로 가공·저장하는 데이터 파운데이션 플랫폼
**역할**: Omni LLM Ops 파이프라인 04 Data Foundation — Omni Model/AI Studio/Document 전 제품에 AI-Ready 데이터 공급
**⚠️ Engine Layer 검토 이슈**: Omni Docu(AIWORKX Docu), Omni OCR(AIWORKX OCR)과 함께 Agent 카테고리 제품이 아닌 별도 Engine 레이어 또는 Data 카테고리 적용 여부 추가 검토 필요 (Agent Category v2r2 섹션 4 참조)

**네이밍 후보 검토 결과**:

| 순위 | 후보명 | 최종 AIWORKX 브랜드명 | TM 리스크 | 결과 |
|------|--------|----------------------|----------|------|
| ★ 1순위 | **DataMill** | AIWORKX DataMill | ⚠️ 주의 (data.mill·Data Mill 글로벌 다수, 한국 충돌 없음) | KIPRIS Class 42 법무팀 확인 후 확정 |
| 2순위 | RawFlow | AIWORKX RawFlow | ⚠️ 주의 (경미한 유사명, 동일 업종 없음) | DataMill TM 이슈 시 대체 |
| 탈락 | DataSmith | — | 🔴 위험 | DATASMITH AI SOLUTIONS Pvt. Ltd.(인도) Generative AI 직접 충돌 |

**파이프라인 시너지**: DataMill(가공) → QualScan(검증) → Docs/Index(색인) 3단 파이프라인 스토리 성립

**최종 추천**:
- 1순위: **AIWORKX DataMill** — Mill(제분소) 은유로 비정형→AI-Ready 가공 의미 직관적, 한국 충돌 없음 (KIPRIS 확인 후 확정)
- 2순위: **AIWORKX RawFlow** — 파이프라인 흐름 강조, 상표 클린

**다음 단계**: DataMill KIPRIS Class 42 법무팀 정식 조회 → Brand Governance NRB 등록 → Engine Layer 위치 결정 (Agent Category v2r2 피드백 연동)

**SharePoint**: [Data_Blackolive_네이밍검토_20260331_v3.docx](https://testworks.sharepoint.com/sites/aiworkx-/Shared%20Documents/네이밍%20검토/Data/Blackolive_20260331/Data_Blackolive_네이밍검토_20260331_v3.docx)

---

## TedWorks — Test 사업부 (최신: v2, 2026-03-26)

**솔루션명 (가칭)**: TedWorks
**핵심 기능**: SW/SoC/App V&V(검증·확인) 자동화 솔루션 — AI 반도체·차량용 SoC Intelligent Board Farm 기반 대용량 테스트 자동화
**ToD™ 탑재**: Q.One 연동 → 반복 테스트 자동 스케줄링 / Powered by ToD™ 표기 필수

**네이밍 후보 검토 결과**:

| 후보명 | 최종 AIWORKX 브랜드명 | 결과 | 비고 |
|--------|----------------------|------|------|
| TestFarm | AIWORKX TestFarm | ✅ **1순위** | Test(기능)+Farm(핵심 아키텍처 'Intelligent Board Farm' 직결), KIPRIS 조회 필요 |
| FarmProbe | AIWORKX FarmProbe | ✅ **2순위** | Probe 기등재 토큰, KIPRIS·SNS·경쟁사 클린, TestFarm TM 이슈 시 즉시 대체 |
| SystemProbe | AIWORKX SystemProbe | ✅ **3순위** | V&V 전문성 직접 표현, 범용 포지셔닝 적합 |
| AutoBench | AIWORKX AutoBench | ⚠️ 후보 | 오픈소스 동명 도구 존재 — 주의 |
| SiliconBench | — | ❌ 탈락 | 반도체 한정 포지셔닝, 확장성 부족 |
| DevBench | — | ❌ 탈락 | 개발자 도구 연상, V&V 포지셔닝 불명확 |

**최종 추천**:
- 1순위: **AIWORKX TestFarm** — Test+Farm으로 제품 본질 가장 직관적 표현, 2음절 간결성 (KIPRIS 조회 후 확정)
- 2순위: **AIWORKX FarmProbe** — TestFarm TM 리스크 발생 시 즉시 대체 확정

**다음 단계**: TestFarm KIPRIS 클래스 9·42 상표 조회 → 클린 확인 시 NRB 즉시 상정

**SharePoint**: [Test_TedWorks_네이밍검토_20260326_v2.docx](https://testworks.sharepoint.com/sites/aiworkx-/Shared%20Documents/네이밍%20검토/Test/TedWorks_20260326_v2/Test_TedWorks_네이밍검토_20260326_v2.docx)

---

## Agent Category — 5개 솔루션 한꺼번에 (최신: v2r6, 2026-04-01) ✅ 최종 확정

**검토 대상**: Omni AI 브랜드 → AIWORKX Agent 카테고리 전환
**상태**: **v2r6 최종 확정** (2026-04-01) — 향후 네이밍 검토 시 이 문서를 기준으로 사용

### TM 조사 결과 및 확정 네이밍

| 기존명 (Omni) | 현행 | TM 리스크 | 확정 추천 | TM 리스크 | 비고 |
|--------------|------|----------|----------|----------|------|
| Omni AI Studio | ~~AIWORKX Studio~~ | 🔴 DROP | **AIWORKX Forge** | 🟡 주의 | Honeywell Forge·Mistral Forge — 법무팀 KIPRIS 조회 필요 |
| Omni AI API | ~~AIWORKX Connect~~ | 🔴 DROP | **AIWORKX Relay** | 🟡 주의 | Relay.app AI 자동화 SaaS — 법무팀 KIPRIS 조회 필요 |
| Omni AI Center | AIWORKX Center | 🟡 주의 | **AIWORKX Care** ★1순위 | 🟢 안전 | Center는 Amazon Connect 연상, Care는 클린 |
| Omni Document (RAG) | AIWORKX Docu | 🟢 안전 | **AIWORKX Ingest** ★1순위 | 🟢 안전 | Docu 브랜드성 부족 — Ingest가 RAG E2E 파이프라인 포괄 |
| Omni OCR | AIWORKX OCR | 🟡 주의 | **AIWORKX Lens** ★1순위 | 🟢 안전 | OCR 범용기술용어, MS Lens 종료 확인 — Lens 클린 |

**⛔ DROP 메모**:
- ~~AIWORKX Studio~~ — Microsoft Copilot Studio 동일 업종 직접 충돌 (🔴). Forge로 대체.
- ~~AIWORKX Connect~~ — MuleSoft Anypoint Connect 동일 업종 직접 충돌 (🔴). Relay로 대체.

**카테고리 구조 결정**:
- Omni Docu (AIWORKX Ingest) / Omni OCR (AIWORKX Lens): **Agent 카테고리 유지** (Option A 채택)
- Engine 레이어 신설(Option C) 삭제 — Ingredient Tech는 **AXDC™(ToD™ 기반) 단일 체계**로 운영

**최종 추천 요약**:
- AIWORKX Forge (🟡) — Studio 대체, No-Code Agent 빌더 (KIPRIS 법무팀 확인 필요)
- AIWORKX Relay (🟡) — Connect 대체, API 연동·중계 (KIPRIS 법무팀 확인 필요)
- **AIWORKX Care** (🟢) — Center 대체, AICC 고객 케어 ★즉시 사용 가능
- **AIWORKX Ingest** (🟢) — Docu 대체, RAG 파이프라인 ★즉시 사용 가능
- **AIWORKX Lens** (🟢) — OCR 대체, IDP 문서 인식 ★즉시 사용 가능

**다음 단계**: Forge·Relay KIPRIS Class 42 법무팀 정식 조회 → NRB 상정 → Care·Ingest·Lens 즉시 NRB 상정 가능

**SharePoint (v2r6, 최종)**: [Agent_AgentCategory_네이밍검토_20260401_v2r6.docx](https://testworks.sharepoint.com/sites/aiworkx-/_layouts/15/Doc.aspx?sourcedoc=%7B6BE9AAC4-D22C-46B2-885C-4B2384505171%7D&file=Agent_AgentCategory_%EB%84%A4%EC%9D%B4%EB%B0%8D%EA%B2%80%ED%86%A0_20260401_v2r6.docx&action=default&mobileredirect=true)

**SharePoint (v1, 2026-03-30)**: [Agent_AgentCategory_네이밍검토_20260330.docx](https://testworks.sharepoint.com/sites/aiworkx-/Shared%20Documents/네이밍%20검토/Agent/AgentCategory_20260330/Agent_AgentCategory_네이밍검토_20260330.docx)

---

## Agent Category 신규 솔루션 — 8개 (최신: v3, 2026-04-01)

**검토 대상**: Agent Category 신규 솔루션 8개 (v2r6 별도 문서)
**상태**: 현업 피드백 요청 중 — 모든 신규 토큰 Rule 4 NRB 상정 필요

### 네이밍 추천 요약 (WebSearch TM 조사 완료)

| 솔루션 (가칭) | ★ 1순위 | TM | 2순위 | TM | ⛔ DROP |
|-------------|--------|-----|------|-----|--------|
| 기업카드 발급 심사 Agent | **AIWORKX Screen** | 🟢 | AIWORKX Verdict | 🟡 | ~~Assess~~ 🔴 |
| IT 코드 리뷰 Agent | **AIWORKX DevProbe** | 🟢 | AIWORKX CodeTrace | 🟢 | — |
| 유통 물류 콜봇 | **AIWORKX RouteCall** | 🟢 | AIWORKX FreightCall | 🟢 | ~~Dispatch~~ 🔴 |
| LLM 챗봇 | **AIWORKX Thread** | 🟢 | AIWORKX Chat | 🟡 | ~~Dialog~~ 🔴 ~~Converse~~ 🔴 |
| 행정 민원 AI | **AIWORKX GovDesk** | 🟢 | AIWORKX CivicServe | 🟢 | ~~Civic~~ 🔴 |
| AI 심사 자동화 | **AIWORKX Adjudge** | 🟢 | AIWORKX Screen | 🟢 | ~~Triage~~ 🔴 |
| 정책 데이터 분석 | **AIWORKX Radar** | 🟢 | AIWORKX Prism | 🟢 | ~~Foresight~~ 🔴 ~~Signal~~ 🔴 |
| 공공 RAG 시스템 | **AIWORKX Corpus** | 🟢 | AIWORKX Archive | 🟢 | ~~Codex~~ 🔴 ~~Lex~~ 🔴 |

**ToD™ 표기 대상 (Powered by AXDC™)**: GovDesk, Adjudge, Corpus

**DROP 사유 요약**:
- ~~Dispatch~~: Bland AI Dispatch·DispatchMVP·VoiceInfra 등 동일 물류 AI 업종 다수 충돌
- ~~Dialog~~: Dialog.ai $4.4M 시드펀딩 AI 에이전트 동일 업종
- ~~Converse~~: Converse AI by Cerebro·Conversed.ai 등록 상표 다수
- ~~Civic~~: Civic AI Inc. LinkedIn 등재, CivicPlus 정부 AI 솔루션 동일 업종
- ~~Triage~~: CLARA Triage·OverseeAI Claims Triage·Sirion AI Underwriting Triage 보험 AI 다수
- ~~Foresight~~: foresightai.ai·foresight.ai·ForesightIQ 다수 직접 충돌
- ~~Signal~~: Signal AI (영국 상장사, 레퓨테이션 관리 AI 전문기업) 직접 충돌
- ~~Codex~~: OpenAI Codex 주간 활성 200만+ 절대 충돌
- ~~Lex~~: Lextar AI·LexisNexis Lexis+ 법률 AI 직접 충돌

**다음 단계**: 현업 선택 확정 → 법무팀 KIPRIS Class 42 정식 조회 → NRB 상정

**SharePoint (v3)**: [Agent_AgentCategory_신규솔루션_네이밍검토_20260401_v3.docx](https://testworks.sharepoint.com/sites/aiworkx-/_layouts/15/Doc.aspx?sourcedoc=%7B246D2DB0-D9F2-403E-8560-A0307E427789%7D&file=Agent_AgentCategory_%EC%8B%A0%EA%B7%9C%EC%86%94%EB%A3%A8%EC%85%98_%EB%84%A4%EC%9D%B4%EB%B0%8D%EA%B2%80%ED%86%A0_20260401_v3.docx&action=default&mobileredirect=true)
