# 네이밍 검토 이력

> **관리 원칙**: SharePoint 최신 발행 문서 기준으로 유지. 버전 업데이트 시 이 파일도 동기화할 것.

---

## CodeReview 확장 — Agent 사업부 (최신: v1 draft, 2026-04-28) ★최신 — KB금융 RFI 대응 + 역할 확장 (코드 리뷰 + Text-to-SQL + 온톨로지)

**솔루션명 (가칭)**: Code Review (확장) — 기존 IT 코드 리뷰 Agent 역할 확장
**핵심 기능**: 코드 리뷰 + 코드 분석 + Text-to-SQL + 기업 특화 온톨로지 + 멀티 에이전트 플랫폼. 현업↔IT 소통 가속, 금융권/기간계 분리, 샌드박스 보안, 제조·금융 도메인 특화. C#·COBOL 등 레거시 지원 + 로컬 LLM 옵션.
**AxDC™ 탑재**: ✅ Powered by AxDC™ 표기 필수 (Ontology + ToD = AxDC)
**참고 RFI**: KB금융지주 Code Review Agent 기술 검증 정보제공요청서 (2026-02-27 마감)
**이전 검토**: Agent_AgentCategory_신규솔루션_네이밍검토_20260401_v3.docx — IT 코드 리뷰 Agent → DevProbe(1순위) / CodeTrace(2순위)

**⛔ 사용자 제안 후보 검토 결과**:
- ~~DevBridge~~ — DROP. 사유: Devbridge(시카고 SW 컨설팅, Cognizant Softvision 2021 인수, USPTO 등록상표) 직접 충돌
- ~~CodeBridge~~ — DROP. 사유: codebridge.tech / bridge-defense.com/codebridge / codebridgesoftware.com / codebridgehq.com / codebridge.info — 5+ 동일 업종 포화
- WorkBridge — 🟡 주의. Workbridge Associates(Motion Recruitment IT 스태핑) IT 인접

**⛔ 신규 탐색 추가 DROP (8개)**: BizBridge(bizbridge.io AI 거래) / CodeMesh(codemeshmcp.com 멀티에이전트) / CodeWeave(codeweave.co GenAI Stacks, Patent Pending) / CodeAtlas(코드 의존성 시각화) / CodeNexus(VSCode LLM ext + Code Nexus Helsinki) / CodeAxis(codeaxis.ai 의료코딩) / AxCode(Siemens AX Code + AX Platform) / CodeFort(codefortify.ai 코드 보안 + codefort.com SaaS) / AskCode(askcode.org + AskCodebase) / DevWeaver(Weaver AI $55M)

**네이밍 후보 검토 결과 (v1)**:

| 순위 | 후보 | 최종 AIWORKX 브랜드명 | TM 리스크 | NRB 경로 | 결과 |
|------|------|----------------------|----------|---------|------|
| ★ 1순위 | **ReqBridge** | AIWORKX ReqBridge | 🟢 안전 | Req·Bridge 신규 토큰 등재 NRB | RFI 양 축(요구사항+코드) 직결, Bridge 패밀리 中 유일 클린 |
| 2순위 | **DevProbe** | AIWORKX DevProbe | 🟢 안전 | 기등재(2026-04-01 v3) — NRB 즉시 상정 | KB RFI 일정 대응 가장 빠른 경로, Probe 패밀리 일관성 |
| 3순위 | **CodeRigor** | AIWORKX CodeRigor | 🟡 주의 | Rigor 신규 토큰 등재 NRB (AgentRigor 시리즈) | testRigor(코드리스 테스트 자동화) 인접 카테고리 인지 혼동 우려 |
| 대안 | CodeTrace | AIWORKX CodeTrace | 🟢 안전 | Trace 등재 토큰 — NRB 즉시 상정 | v3 2순위 검토 완료 |
| 대안 | WorkBridge | AIWORKX WorkBridge | 🟡 주의 | Work·Bridge 신규 토큰 NRB | Workbridge Associates IT 스태핑 인접 |

**최종 추천 (v1)**:
- 1순위: **AIWORKX ReqBridge** /렉브릿지/ — RFI 양 축(요구사항 Review Agent + Code Review Agent) 직결, Bridge 패밀리 中 유일 글로벌 클린, 회사 핵심 가치 ‘현업↔IT 소통 가속’과 alignment
- 2순위: **AIWORKX DevProbe** /데브프로브/ — 2026-04-01 v3 1순위 확정, NRB 즉시, KB RFI 일정 대응 최적
- 3순위: **AIWORKX CodeRigor** /코드리거/ — AgentRigor 시리즈 일관성, Rigor 패밀리 구축 (testRigor 인지 주의)

**KIPRIS WebSearch 사전 조회 결과 (2026-04-28)**:
- ReqBridge: 🟢 안전 — 동명 미발견, reqbridge.com/.ai/.io 도메인 점유 미확인
- DevProbe: 🟢 안전 — v3 검토에서 안전 확인
- CodeRigor: 🟡 주의 — 동명 미발견, testRigor(Generative AI 테스트 자동화) Rigor 토큰 활성 사용
- CodeTrace: 🟢 안전 — Trace 등재 토큰
- WorkBridge: 🟡 주의 — Workbridge Associates IT 스태핑 인접

**KIPRIS 조회 링크**:
- [ReqBridge KIPRIS 조회](https://www.kipris.or.kr/srch/srchList.jsp?searchString=ReqBridge&tab=trademark)
- [CodeRigor KIPRIS 조회](https://www.kipris.or.kr/srch/srchList.jsp?searchString=CodeRigor&tab=trademark)
- [WorkBridge KIPRIS 조회](https://www.kipris.or.kr/srch/srchList.jsp?searchString=WorkBridge&tab=trademark)

**다음 단계**:
1. [05-02] 사업부 PO 최종 후보 선택 (ReqBridge / DevProbe / CodeRigor)
2. [05-05] 변리사 정식 출원 검토 의뢰 (KIPRIS Class 9·42, KIPRIS WebSearch 사전 조사 완료 기반)
3. [05-05] [법무팀] CodeRigor — testRigor 상표 혼동 가능성 정밀 검토 (선택 시)
4. [05-05] [법무팀] ReqBridge — Bridge 패밀리 글로벌(USPTO·EUIPO) 출원 가능성 검토
5. [05-05] 도메인 선점 검토 (reqbridge.ai / .com / .io)
6. [05-12] 변리사 결과 수신 → NRB 상정
7. [05-15] Brand Governance 레지스트리 업데이트 + 경영진 승인

**SharePoint (v1 ★최신)**: 업로드 예정 — `네이밍 검토/Agent/CodeReviewExt_20260428/Agent_CodeReviewExt_네이밍검토_20260428_v1.docx`
> ⚠️ 본 v1 draft는 SharePoint 업로드 전 상태로 git에 선반영. 업로드 완료 후 SharePoint 링크와 함께 v1 final로 갱신 예정.

---

## AAEF — Test 사업부 (최신: v3, 2026-04-02) ★최신

**솔루션명 (가칭)**: AAEF (AI Agent Evaluation Framework)
**핵심 기능**: AI 에이전트 신뢰성·성능 자동 평가 프레임워크
**⚠️ 가칭 충돌 주의 1**: RagaAI가 'AAEF(Agentic Application Evaluation Framework)'를 공식 브랜드로 사용 중 → 외부 표기·마케팅에 가칭 AAEF 사용 금지
**🚨 신규 충돌 경고 (v3, 2026-04-02)**: Akto가 'Agent Probe'를 에이전틱 AI 자동화 레드팀 엔진으로 2025.12 공개·운영 중 → AgentProbe 1순위 → ⚠️ 조건부 보류 변경. EvalProbe 1순위 승격.

**네이밍 후보 검토 결과 (v3)**:

| 후보명 | 최종 AIWORKX 브랜드명 | 결과 | 비고 |
|--------|----------------------|------|------|
| AgentProbe | AIWORKX AgentProbe | ⚠️ **조건부 보류** | Akto 'Agent Probe' 2025.12 동일명 선사용 — 국내 단기 사용 가능, 글로벌 출원 리스크 |
| EvalProbe | AIWORKX EvalProbe | ✅ **1순위 (v3 승격)** | Eval+Probe 조합, 기술적 정확성 우수, Akto 충돌 없음 |
| TrustProbe | AIWORKX TrustProbe | ✅ **2순위** | Trust 키워드, 금융·공공 고객 공감도 높음 |
| ReliProbe | AIWORKX ReliProbe | ✅ **3순위** | Reliability 차별점 명확 |
| AgentAudit | — | ❌ 탈락 | 미국 상표 충돌 위험 |
| AgentGuard | — | ❌ 탈락 | 주요 경쟁사 다수 사용 중 |
| AgentBench | — | ❌ 탈락 | Tsinghua THUDM ICLR 2024 논문·GitHub 브랜드 충돌 |

**최종 추천 (v3)**:
- 1순위: **AIWORKX EvalProbe** — Akto 충돌 없음, 네이밍 아키텍처 원칙에 적합, Probe 시리즈 일관성
- 2순위: **AIWORKX TrustProbe** — AI 신뢰성 직결, 금융·공공 특화 포지셔닝

**KIPRIS WebSearch 사전 조회 결과 (2026-04-07)**:
- EvalProbe: 🟢 안전 — 동일명 미발견, 조어(Eval+Probe) 독창성 높음
- TrustProbe: 🟢 안전 — 동일명 미발견

**다음 단계**: 변리사 EvalProbe·TrustProbe KIPRIS Class 42 정식 조회 의뢰 → NRB 상정 (EvalProbe 1순위·TrustProbe 대안)

**SharePoint (v3 ★최신)**: [Test_AAEF_네이밍검토_20260402_v3.docx](https://testworks.sharepoint.com/sites/aiworkx-/_layouts/15/Doc.aspx?sourcedoc=%7BAF3896F9-B767-4DFF-9D1F-544F0CBCF43E%7D&file=Test_AAEF_%EB%84%A4%EC%9D%B4%EB%B0%8D%EA%B2%80%ED%86%A0_20260402_v3.docx&action=default&mobileredirect=true)

**SharePoint (v2)**: [Test_AAEF_네이밍검토_20260331.docx](https://testworks.sharepoint.com/sites/aiworkx-/Shared%20Documents/네이밍%20검토/Test/AAEF_20260331/Test_AAEF_네이밍검토_20260331.docx)

---

## Q One — Test 사업부 (최신: v4-1, 2026-04-10) ★최신 — Intelliq DROP + QualScan 1순위 승격

**솔루션명 (가칭)**: Q One (AI 기반 UX/UI 테스트 + API 테스트 + 데이터 검증 + 지식 자산화 + Action Flow Map)
**브랜드 포지션**: AUTONOMOUS QA
**핵심 기능**: 비즈니스 문서 기반 테스트 설계, 좌표 기반 추출·매핑, Action Flow Map(서비스 구조 시각화), Full-Spectrum QA(UI+API+Data 통합)
**PO 키워드 요청**: Intelligence(지능형) · Autonomous(자율성) · Foundation(품질 근간)
**⚠️ v3 재검토 사유**: 솔루션 PO UIProbe 피드백 — "UI 영역 한정 인식, API·데이터 검증 확장성 미반영"
**🔄 v4 변경사항 (2026-04-08)**: Autonomous QA 정체성 반영 신규 후보 4개 추가 (Intelliq, QualScan, Qualitiq, TestIQ) + AI QA 시장·경쟁사 분석 추가
**🚨 v4-1 변경사항 (2026-04-10)**: Intelliq 상표권 심각한 충돌 발견 → 즉시 DROP. QualScan 1순위 승격.

**⛔ DROP 확정 메모**:
- ~~AIWORKX Sentinel~~ — DROP. 사유: Microsoft Sentinel(SIEM)·SentinelOne(보안)·Sentinel AI(CI/CD) AI/SW 다수 충돌
- ~~AIWORKX AppBench~~ — DROP. 사유: appbench.ai(YC 기반) 충돌
- ~~AIWORKX SceneScan~~ — DROP. 사유: Nerian Vision 등록 상표 충돌
- ~~AIWORKX Intelliq~~ — **DROP (v4-1, 2026-04-10)**. 사유: (1) Excellarate/Encora "IntelliQ™" QA 테스트 자동화 프레임워크 — 동일 업종 직접 충돌 (2) IntelliQA Ltd(UK) 테스트 자동화 기업 — 동일 업종 (3) GlobalLogic "InteliQ" AI QA 솔루션 — 동일 업종 (4) USPTO LIVE 등록상표 "INTELLIQ" (The Wisory Inc.) (5) intelliq.com 등 모든 도메인 점유 (6) 전 세계 15개+ 기업/제품이 IntelliQ/InteliQ 사용 중 — 브랜드 완전 포화

**네이밍 후보 검토 결과 (v4 — 전체 9개)**:

| # | 후보명 | 최종 AIWORKX 브랜드명 | 결과 | TM 리스크 | 비고 |
|---|--------|----------------------|------|----------|------|
| ~~★1~~ | ~~Intelliq~~ | ~~AIWORKX Intelliq~~ | ⛔ **DROP (v4-1)** | 🔴 위험 | Excellarate "IntelliQ™" QA동일업종 + IntelliQA(UK) 테스트자동화 + USPTO LIVE등록 + 15개+기업 사용 — 브랜드 포화 |
| ★1 | **QualScan** | AIWORKX QualScan | ✅ **1순위 (v4-1 승격)** | 🟢 안전 | Quality+Scan, Qual·Scan 모두 기등재 토큰 → NRB 즉시 상정 가능, 가장 빠른 실행 경로 |
| 2 | Scrutiq | AIWORKX Scrutiq | ✅ **2순위 (v4-1 승격)** | 🟢 안전 | Scrutiny+IQ 조어, Intelligence 키워드 강력, 신규 토큰 NRB 필요 |
| 4 | Qualitiq | AIWORKX Qualitiq | 🔄 검토 중 (v4 신규) | 🟢 안전 | Quality+IQ 조어, Intelligence·Quality 충족 |
| 5 | TestIQ | AIWORKX TestIQ | 🔄 검토 중 (v4 신규) | 🟢 안전 | Test+IQ, Intelligence 충족, 발음/기억성 우수 |
| 6 | QualProbe | AIWORKX QualProbe | 🔄 검토 중 (v3) | 🟢 안전 | Quality+Probe, 기등재 토큰, Intelligence 키워드 미충족 |
| 7 | UIProbe | AIWORKX UIProbe | ⏸️ 하향 (v3→v4) | 🟡 주의 | PO "UI 한정" 피드백 + uiprobe.io 충돌 |
| 8 | AutoProbe | AIWORKX AutoProbe | 🔄 검토 중 (v3) | 🟡 주의 | Autonomous+Probe, AgRobotics AutoProbe(농업) 유사 |
| 9 | Assurai | AIWORKX Assurai | 🔄 검토 중 (v3) | 🟡 주의 | Assure+AI, AssurAI 데이터셋(학술) AI 도메인 |
| — | IntentProbe | AIWORKX IntentProbe | ⏸️ 보류 (v2→v3) | 🟢 안전 | PO "UI 한정" 피드백으로 우선순위 하향 |
| — | FlowProbe | AIWORKX FlowProbe | ⏸️ 보류 (v2→v3) | 🟢 안전 | 품질 전 영역 포괄성 부족 |

**최종 추천 (v4-1, Intelliq DROP 후 재조정)**:
- 1순위: **AIWORKX QualScan** /퀄스캔/ — Qual+Scan 기등재 토큰 → NRB 즉시 상정, 제품 3대 필러(문서 스캔·추출 매핑·UI 스캔) 포괄
- 2순위: **AIWORKX Scrutiq** /스크루티큐/ — Scrutiny+IQ 조어, Intelligence 키워드 강력, 신규 토큰 NRB 필요
- 3순위: **AIWORKX Qualitiq** /퀄리티큐/ — Quality+IQ 조어, Intelligence·Quality 모두 충족

**시장 분석 (v4 추가)**:
- Gartner 2028 전망: 기업 70%가 AI-Augmented Testing 도구 SDLC 통합 (2025 초 20%)
- Forrester 2025 Q4: "Autonomous Testing Platforms" Wave 최초 발행
- 경쟁사: testRigor, Applitools Autonomous, Functionize, Virtuoso QA, mabl, Katalon 등 — 대부분 조어형 네이밍 사용
- Q One 고유 차별점: Knowledge Repo(문서→테스트 지식 변환), Action Flow Map(서비스 구조 시각화), Full-Spectrum QA

**다음 단계**:
1. [04-14] 사업부 PO 후보 선택 (QualScan / Scrutiq / Qualitiq / 기타) — ⚠️ Intelliq DROP됨
2. [04-14] 선택 후보 변리사 KIPRIS Class 42 정식 조회 의뢰
3. [04-21] 변리사 결과 수신 → NRB 상정
4. [04-25] Brand Governance 레지스트리 업데이트 + 경영진 승인

**SharePoint (v4 ★최신)**: 업로드 대기 중

**SharePoint (v3)**: [Test_QOne_네이밍검토_20260406_v3.docx](https://testworks.sharepoint.com/sites/aiworkx-/_layouts/15/Doc.aspx?sourcedoc=%7B0230447C-9E8D-4F94-AA62-B921ED20EADF%7D&file=Test_QOne_%EB%84%A4%EC%9D%B4%EB%B0%8D%EA%B2%80%ED%86%A0_20260406_v3.docx&action=default&mobileredirect=true)

**SharePoint (v2)**: [Test_QOne_네이밍검토_20260331.docx](https://testworks.sharepoint.com/sites/aiworkx-/Shared%20Documents/네이밍%20검토/Test/QOne_20260331/Test_QOne_네이밍검토_20260331.docx)

---

## ToD™ — Technology Ingredient Brand (최신: v3 rev.5, 2026-04-06) ★최신

**검토 대상**: AIWORKX 기술 인그리디언트 브랜드 `ToD™` (Powered by ToD™ 표기용)
**현행 정의**: Task-oriented Deterministic AI

**검토 경과**:

| 회차 | 날짜 | 주요 내용 |
|------|------|----------|
| v1 | 2026-03-20 | Linea™·Axia™ 제안 → AX prefix 전략 전환 결정 |
| v2 | 2026-03-26 | AXO/AXON/AXEN 검토 → 상표·업종 충돌 탈락 |
| v3 | 2026-03-30 | AXDO™ 1순위 확정, AXDC™ 신규 추가 (4순위) |
| v3 rev.3 | 2026-03-31 | AXDC™ 1순위 승격, AXDO™ 2순위로 조정 |
| v3 rev.4 | 2026-03-31 | AXDC™ KIPRIS/TM 가조사 완료 (변리사 정식 조회 예정) |
| **v3 rev.5** | **2026-04-06** | **KIPRIS 변리사 조회 결과 확인 (6개 전종). AXGO™ USPTO 주의 발견. 최종 순위 확정.** |

**v3 rev.5 후보 순위 (KIPRIS 변리사 조회 완료, 2026-04-06)**:

| 순위 | 후보 | 발음 | 풀네임 | KIPRIS 결과 | TM 판정 |
|------|------|------|--------|------------|--------|
| ★ 1순위 | **AXDC™** | /에이엑스-디씨/ | AX+DC (Direct Compute / AC→DC 메타포) | **0건** — 동일·유사 완전 클린 | 🟢 안전 |
| 2순위 | AXDO™ | /에이엑스-두/ | AX+DO (실행·완수) | 14건 (국내5+해외9), 업종 무관 | 🟢 클린 |
| 3순위 | AXHIT™ | /에이엑스-힛/ | AX+HIT (목표 명중·달성) | 1건 (MAXHIT, Cl.012 — 업종 다름) | 🟢 클린 |
| ⚠️ 4순위 | AXGO™ | /에이엑스-고/ | AX+GO (실행 개시) | 48건 (국내26+해외22), USPTO "AXGO" Cl.009 등록 1건 [NEW] | 🟠 주의 |
| 5순위 | AXRUN™ | /에이엑스-런/ | AX+RUN (작동·실행) | 10건 (국내6+해외4), 업종 무관 | 🟢 클린 |
| 6순위 | AXSET™ | /에이엑스-셋/ | AX+SET (완료·세팅) | 6건 (국내1+해외5), 업종 무관 | 🟢 클린 |

**⚠️ 주요 주의사항**:
- **AXDC™**: AC/DC 록밴드 연상 → 보수적 엔터프라이즈(금융·공공) 이미지 부담 가능. 법무팀 AC/DC 상표 혼동 가능성 사전 확인 필수
- **AXGO™**: USPTO Class 009 등록상표 1건 (Xiao Jun Zhou) 발견 → 글로벌 출원 시 저촉 위험. 국내 출원은 클린

**탈락 후보 누적 (v1~v3, 총 12개)**: AXO, AXON, AXEN, AXCO, AXFIN, AXEND, AXMIT, AXIM, AXIVE, AXEVO, AXELO, AXWORK

**최종 추천 (v3r5)**:
- 1순위: **AXDC™** — KIPRIS 0건 완전 클린, AC/DC 이중 레이어 의미(기술적·전략적), 브랜드 임팩트 우위
- 2순위: **AXDO™** — 실행·완수 직관적, 상표 클린, 즉시 출원 가능

**다음 단계**:
- ① [법무팀] AXDC™ AC/DC 상표 혼동 가능성 최종 검토
- ② [법무팀] AXDC™ KIPRIS Class 42 변리사 정식 출원 의뢰
- ③ [주의] AXGO™ USPTO Class 009 저촉 여부 — 글로벌 출원 전 법무팀 검토 필요
- ④ [경영진] AXDC™ 확정 시 NRB 1순위 상정
- ⑤ [확정 후] Brand Governance Token System 등록

**SharePoint (v3r5 ★최신)**: [기타_ToD_네이밍검토_20260406_v3r5.docx](https://testworks.sharepoint.com/sites/aiworkx-/Shared%20Documents/네이밍%20검토/4.%20기타%20-%20ToD/ToD_20260330_v3/기타_ToD_네이밍검토_20260406_v3r5.docx)

**SharePoint (v3r3)**: [기타_ToD_네이밍검토_20260331_v3r3.docx](https://testworks.sharepoint.com/sites/aiworkx-/Shared%20Documents/네이밍%20검토/기타/ToD_20260330_v3/기타_ToD_네이밍검토_20260331_v3r3.docx)

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

**KIPRIS WebSearch 사전 조회 결과 (2026-04-07)**:
- DataMill: 🟡 주의 — datamill.co(데이터 분석), datamillsoftware.com(MS Dynamics, 1998년 설립), datamill.solutions(독일, 데이터 품질) — 한국 직접 충돌 미확인이나 글로벌 SW 다수 사용
- RawFlow: 🟡 주의 — 경미한 유사명, 동일 업종 없음

**다음 단계**: 변리사 DataMill KIPRIS Class 42 정식 조회 의뢰 → Brand Governance NRB 등록 → Engine Layer 위치 결정 (Agent Category v2r2 피드백 연동)

**SharePoint**: [Data_Blackolive_네이밍검토_20260331_v3.docx](https://testworks.sharepoint.com/sites/aiworkx-/Shared%20Documents/네이밍%20검토/Data/Blackolive_20260331/Data_Blackolive_네이밍검토_20260331_v3.docx)

---

## TedWorks — Test 사업부 (최신: v4, 2026-04-08) ★최신 — V&V Farm·V-Farm·DeviceProbe 추가 검토

**솔루션명 (가칭)**: TedWorks
**핵심 기능**: SW/SoC/App V&V(검증·확인) 자동화 솔루션 — AI 반도체·차량용 SoC Intelligent Board Farm 기반 대용량 테스트 자동화
**ToD™ 탑재**: Q.One 연동 → 반복 테스트 자동 스케줄링 / Powered by ToD™ 표기 필수

**⚠️ WebSearch 상표권 재조회 결과 (2026-04-02)**:

| 후보명 | TM 리스크 | 조회 결과 |
|--------|----------|----------|
| TestFarm | 🔴 위험 | testfarm.org ("Test Automation for HMI and Embedded Software") 운영 중 / GitHub testfarm 조직 / SourceForge 배포 / SEGGER Knowledge Base 등재 — 동일 업종(임베디드 소프트웨어 테스트 자동화) 직접 충돌 |
| FarmProbe | 🟢 안전 | 동일/유사명 사용 없음 — KIPRIS Class 42 법무팀 최종 확인 권고 |
| SystemProbe | 🟢 안전 | 동일/유사명 사용 없음 (SOFTPROBE는 다른 명칭) — KIPRIS Class 42 법무팀 최종 확인 권고 |
| AutoBench | 🔴 위험 | autobench.org (AI LLM 벤치마크 플랫폼 운영 중) / GitHub AutoBench 조직 / 오픈소스 LLM testbench generator — 동일 업종(AI 소프트웨어 테스트·평가) 직접 충돌 |

**⛔ DROP 메모**:
- ~~AIWORKX TestFarm~~ — testfarm.org 동일 업종(임베디드 SW 테스트 자동화) 직접 충돌 (🔴). FarmProbe로 즉시 대체.
- ~~AIWORKX AutoBench~~ — autobench.org AI 벤치마크 플랫폼 + GitHub AutoBench 조직 동일 업종 충돌 (🔴). DROP 확정.

**네이밍 후보 최종 결과 (v3 + 2026-04-07 대안 추가 검토)**:

| 후보명 | 최종 AIWORKX 브랜드명 | 결과 | TM 리스크 |
|--------|----------------------|------|----------|
| ~~TestFarm~~ | — | ⛔ DROP | 🔴 위험 — testfarm.org 동일 업종 충돌 |
| FarmProbe | AIWORKX FarmProbe | ✅ **1순위** | 🟢 안전 — Probe 기등재 토큰, KIPRIS WebSearch 안전 확인 (2026-04-07) |
| DeviceProbe | AIWORKX DeviceProbe | ✅ **2순위 (2026-04-07 신규)** | 🟢 안전 — Probe 기등재 토큰, SoC/디바이스 테스트 직관적, KIPRIS WebSearch 안전 확인 |
| SystemProbe | AIWORKX SystemProbe | ✅ **3순위** | 🟡 주의 — Datadog Agent "system-probe" 동일명 컴포넌트 (한국 활동 중), V&V 범용성 장점 |
| ~~AutoBench~~ | — | ⛔ DROP | 🔴 위험 — autobench.org 동일 업종 충돌 |
| ~~SiliconBench~~ | — | ❌ 탈락 | — 반도체 한정 포지셔닝, 확장성 부족 |
| ~~DevBench~~ | — | ❌ 탈락 | — 개발자 도구 연상, V&V 포지셔닝 불명확 |
| ~~V-Farm~~ | — | ⛔ DROP (2026-04-07) | 🔴 위험 — V-Farm(영국 v-farm.co.uk) 수직농업 활성 브랜드 + Rule 2 위반("V" 과도 축약) |
| V&V Farm | AIWORKX V&V Farm | ⏸️ 보류 (2026-04-07) | 🟡 주의 — V&V Farms Inc.(미국 농업) 비동종이나, "V&V" 범용약어 식별력 약함 + Rule 2 부분위반 |

**최종 추천 (v3+)**:
- 1순위: **AIWORKX FarmProbe** — Probe 기등재 토큰, TM 클린, Intelligent Board Farm 아키텍처 직결, NRB 즉시 상정 가능
- 2순위: **AIWORKX DeviceProbe** — Probe 기등재 토큰, TM 클린, SoC/디바이스 HW 테스트 직관적, NRB 즉시 상정 가능
- 3순위: **AIWORKX SystemProbe** — V&V 시스템 전체 포괄, 글로벌 직관적, Datadog system-probe 주의 필요

**KIPRIS 조회 링크**:
- [FarmProbe KIPRIS 조회](https://www.kipris.or.kr/srch/srchList.jsp?searchString=FarmProbe&tab=trademark)
- [SystemProbe KIPRIS 조회](https://www.kipris.or.kr/srch/srchList.jsp?searchString=SystemProbe&tab=trademark)

**다음 단계**:
- ① [이번 주] 변리사 의뢰: FarmProbe·DeviceProbe KIPRIS Class 9 + Class 42 정식 조회
- ② [이번 주] SystemProbe — Datadog 'system-probe' 상표 혼동 가능성 법무팀 검토
- ③ [조회 완료 후] NRB 상정: FarmProbe 1순위·DeviceProbe 대안 병행

**SharePoint (v4 ★최신)**: [Test_TedWorks_네이밍검토_20260408_v4.docx](https://testworks.sharepoint.com/sites/aiworkx-/_layouts/15/Doc.aspx?sourcedoc=%7B230595BC-9816-42CB-BEA7-18C6EC89D73D%7D&file=Test_TedWorks_%EB%84%A4%EC%9D%B4%EB%B0%8D%EA%B2%80%ED%86%A0_20260408_v4.docx&action=default&mobileredirect=true)

**SharePoint (v3)**: [Test_TedWorks_네이밍검토_20260402_v3.docx](https://testworks.sharepoint.com/:w:/s/aiworkx-/IQCzNa3SBHVnSog6atftvRsyAcTS4pKDKJmETMjv-3rQi34)

**SharePoint (v2)**: [Test_TedWorks_네이밍검토_20260326_v2.docx](https://testworks.sharepoint.com/sites/aiworkx-/Shared%20Documents/네이밍%20검토/Test/TedWorks_20260326_v2/Test_TedWorks_네이밍검토_20260326_v2.docx)

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

**KIPRIS WebSearch 사전 조회 결과 (2026-04-07)**:
- **Forge**: 🔴 **위험** — Mistral AI "Forge"(AI 모델 빌더), Honeywell Forge(AI SW), Autodesk Forge(한국 활동 중), theforgeai.com(노코드 AI앱), Forge.AI(NLP), Coforge "Forge-X", USPTO 출원(SN 97358404) — AI/SW 동일 업종 다수 충돌
- **Relay**: 🔴 **위험** — Relay.app(AI 워크플로 자동화 SaaS, 2026 Winter "Best for Operations"), RelayThat(디자인 자동화), RELAYTO(콘텐츠 플랫폼) — AI/SaaS 동일 업종 충돌

**⚠️ Forge·Relay 재검토 필요 (2026-04-07)**:
- Forge·Relay 모두 KIPRIS WebSearch에서 🔴 위험 판정 — Agent v2r6 확정 당시 미확인 사항
- Studio(MS Copilot Studio 충돌)·Connect(MuleSoft 충돌) 이미 DROP → **4개 토큰 모두 충돌**
- 대안 탐색 또는 법무팀 정밀 판단 필요

**최종 추천 요약 (2026-04-07 업데이트)**:
- ~~AIWORKX Forge~~ (🔴 재검토) — AI/SW 업종 다수 충돌, 대안 탐색 필요
- ~~AIWORKX Relay~~ (🔴 재검토) — Relay.app AI SaaS 충돌, 대안 탐색 필요
- **AIWORKX Care** (🟢) — Center 대체, AICC 고객 케어 ★즉시 사용 가능
- **AIWORKX Ingest** (🟢) — Docu 대체, RAG 파이프라인 ★즉시 사용 가능
- **AIWORKX Lens** (🟢) — OCR 대체, IDP 문서 인식 ★즉시 사용 가능

**다음 단계**: Forge·Relay 대안 탐색 또는 법무팀 정밀 검토 → Care·Ingest·Lens 즉시 NRB 상정 가능

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

**SharePoint (통합본 ★최신)**: [Agent_AgentCategory_네이밍검토_통합본_20260401.docx](https://testworks.sharepoint.com/sites/aiworkx-/_layouts/15/Doc.aspx?sourcedoc=%7B586DE29E-A3A8-4DE6-9821-595101D53E03%7D&file=Agent_AgentCategory_%EB%84%A4%EC%9D%B4%EB%B0%8D%EA%B2%80%ED%86%A0_%ED%86%B5%ED%95%A9%EB%B3%B8_20260401.docx&action=default&mobileredirect=true)

---

## As Built — Data 사업부 (최신: v1, 2026-04-01)

**솔루션명 (가칭)**: As Built (건설 현장 블랙박스)
**핵심 기능**: 시공 과정의 모든 데이터(영상·로그·시공기록·안전기록 등)를 AI로 자동 수집·구조화·분석하여 건설 현장과 시설 관리 전반에 활용하는 데이터 파운데이션 플랫폼
**ToD™ 탑재**: ✅ Powered by AXDC™ (ToD™ 기반) 표기 필수

**⛔ 기존 후보 전원 DROP (v1)**:

| 후보명 | 판정 | 탈락 사유 |
|--------|------|---------|
| FieldPrint | 🔴 DROP | Fieldprint Inc.(FBI 인증 신원확인, ISO 9001) + Fieldprint Platform®(농업 지속가능성, 등록상표) |
| BuildTrace | 🔴 DROP | BuildTrace AI(buildtraceai.com) — 건설 AI 변경 인텔리전스 플랫폼, 동일 업종 직접 충돌 |
| SiteLog | 🔴 DROP | sitelog.co / SiteLog Infra(독일 Zech) / site-log.com / SitelogIQ — 건설 업종 4개 기업 사용 |

**신규 후보 검토 결과 (WebSearch TM 조사 완료)**:

| 순위 | 후보명 | 최종 AIWORKX 브랜드명 | TM 리스크 | 결과 |
|------|--------|----------------------|----------|------|
| ★ 1순위 | **SiteProbe** | AIWORKX SiteProbe | 🟢 안전 | Probe 기등재 토큰, KIPRIS WebSearch 안전 확인 (2026-04-07), NRB 즉시 상정 가능 |
| ~~2순위~~ | ~~SiteVault~~ | — | 🔴 **DROP (2026-04-07)** | **Veeva Systems 등록상표** — 임상시험 관리 eISF 플랫폼, 한국 CRO(LSK Global PS) 활동 중, 대형 상장사(NYSE: VEEV) |
| 2순위 | BuildPrint | AIWORKX BuildPrint | 🟡 주의 | build-to-print 범용 용어 존재, 시설 관리 확장 시 범위 제약 |

**⛔ DROP 메모 (2026-04-07 추가)**:
- ~~AIWORKX SiteVault~~ — DROP. 사유: Veeva Systems "SiteVault" 등록상표 (임상시험 사이트 관리 SW), 한국 CRO LSK Global PS 등 국내 사용 중, NYSE 상장 대기업으로 상표 방어력 강함.

**최종 추천 (2026-04-07 업데이트)**:
- 1순위: **AIWORKX SiteProbe** — 상표권 클린 (KIPRIS WebSearch 🟢), Probe 기등재 토큰으로 NRB 즉시 상정 가능, "Site"가 건설+시설 모두 포괄
- 2순위: **AIWORKX BuildPrint** — SiteVault DROP 후 차순위, build-to-print 범용성 주의

**다음 단계**: 변리사 SiteProbe KIPRIS Class 42 정식 조회 의뢰 → 클린 확인 시 NRB 즉시 상정 → Brand Governance 레지스트리 FieldPrint → SiteProbe 업데이트

**로컬 문서**: `Data_AsBuilt_네이밍검토_20260401.docx`
