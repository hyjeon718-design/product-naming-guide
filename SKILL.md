---
name: product-naming-guide
description: AIWORKX 사업부/솔루션 네이밍 검토를 자동화하는 스킬. 사업부명(카테고리)과 솔루션 가칭·역할을 입력하면 브랜드 아키텍처 5대 Golden Rules 기준으로 이름 후보 3~5개를 생성하고, KIPRIS 상표권 조회 링크 + WebSearch 유사 상표 검색 + SNS/경쟁사 브랜드 검색까지 자동 수행. 결과는 SharePoint Word 초안으로 저장하고 이메일로 배포. 다음 중 하나라도 해당하면 반드시 이 스킬을 사용하세요: (1) "네이밍 검토", "이름 추천", "네이밍 후보"가 포함된 요청 (2) "{사업부} {솔루션명} 네이밍" 형식 입력 (3) "완성본 배포해줘" 요청 (4) 제품·솔루션·기술 브랜드 이름을 새로 짓거나 변경할 때 (5) AIWORKX 브랜드 아키텍처 관련 이름 검토.
---

# product-naming-guide

사업부/솔루션별 네이밍 검토를 자동화하는 스킬입니다.
네이밍 아키텍처 기준으로 이름 후보를 생성하고, 상표권 조회 · SNS/Google 유사 브랜드 검색 · 경쟁사 검색까지 수행한 뒤 SharePoint에 폴더를 생성하고 Word 초안을 업로드합니다.

## 실행 순서

### 0단계: 정보 수집

사용자 입력에서 아래 정보를 파악하세요. 누락된 필수 항목은 아래 가이드 질문 형식으로 한 번에 물어보세요.

**필수 3가지 (항상 확인)**:
1. **카테고리** — Test / Agent / Data / Verification / Edu / 기타 중 하나
   - "기타"는 제품명이 아닌 기술 브랜드 검토 (예: ToD™ 같은 Ingredient Brand)
2. **가칭(프로젝트명)** — 현재 내부에서 부르는 이름
3. **역할** — 이 제품/기술이 하는 일 한 줄 설명

**선택**:
- 타겟 고객
- 포지셔닝 키워드
- 기존 제품과의 관계
- 피해야 할 단어/패턴
- **ToD™ 기술 탑재 여부** — "Powered by ToD™" 표기 대상인가요?
  (5대 카테고리의 제품명 검토 시 반드시 확인. 탑재 시 출시 문서에 명시 필요)

정보가 부족할 때 반드시 이 형식으로 질문하세요:
> 네이밍 검토를 시작할게요! 아래를 알려주세요.
>
> 1. **카테고리**: Test / Agent / Data / Verification / Edu / 기타 중 어디에 해당하나요?
> 2. **가칭**: 현재 팀에서 부르는 이름이 있나요? (없으면 없다고 알려주세요)
> 3. **역할**: 이 제품/기술이 하는 일을 한 줄로 설명해주세요.
> 4. **ToD™ 탑재**: 이 제품에 ToD™ 기술이 사용되나요? (Powered by ToD™ 표기 여부 결정에 필요)
>    - 5대 카테고리(Test/Agent/Data/Verification/Edu) 제품만 해당 / "기타"는 건너뜀

---

### 1단계: 네이밍 가이드 참조

`~/Documents/naming architecture/` 폴더의 파일들을 읽어 브랜드 아키텍처 기준을 파악하세요.
- 핵심 파일: `aiworkx_naming_architecture_master_diagram_l_0_l_6.md`, `AIWORKX_Brand_Governance.md`
- 파일이 없으면: "naming architecture 폴더에 파일이 없어요. 자료를 먼저 넣어주세요." 안내 후 중단

---

### 2단계: 이름 후보 생성

가이드 기준에 맞춰 이름 후보 3~5개를 생성하세요.

각 후보별로 제공할 내용:
- 후보명
- 아키텍처 적합성 설명 (한 줄)
- 포지셔닝 특징

---

### 3단계: 상표권 간단 조회 (B-3)

각 후보명에 대해 두 가지 방식으로 상표권을 조회하세요.

#### 3-1. KIPRIS 검색 링크 자동 생성

후보명마다 아래 URL 패턴으로 링크를 생성하세요:

```
https://www.kipris.or.kr/srch/srchList.jsp?searchString={후보명}&tab=trademark
```

출력 형식:
```
🏛️ "{후보명}" 상표 조회: https://www.kipris.or.kr/srch/srchList.jsp?searchString={후보명}&tab=trademark
```

#### 3-2. WebSearch로 유사 상표 확인

각 후보명에 대해 WebSearch로 확인하세요:
- 검색어: `"{후보명}" 상표 trademark`
- 검색어: `"{후보명}" 브랜드 기업`

유사 상표 발견 시 경고:
```
⚠️ "{후보명}" — 유사 상표 발견: {발견 내용}. 법무팀 검토 권장.
```

이상 없으면:
```
✅ "{후보명}" — 검색된 유사 상표 없음 (정식 출원 전 법무팀 최종 확인 권장)
```

---

### 4단계: SNS · Google · 경쟁사 유사 브랜드명 검색 (B-4)

각 후보명에 대해 WebSearch를 활용해 아래 채널을 검색하세요.

#### 4-1. Google 검색
```
"{후보명}" 브랜드 제품
"{후보명}" company product
```

#### 4-2. SNS 검색
```
"{후보명}" site:linkedin.com OR site:twitter.com OR site:instagram.com
"@{후보명}" OR "#{후보명}"
```

#### 4-3. 경쟁사 유사 브랜드명 검색
```
"{후보명}" Microsoft OR Google OR AWS OR Salesforce OR ServiceNow OR SAP
"{후보명}" AI 솔루션 OR SaaS OR 플랫폼
```

#### 4-4. 검색 결과 요약 출력

각 후보명별로 리스크 레벨을 표시하세요:

| 채널 | 결과 | 리스크 |
|------|------|--------|
| Google | 동일명 사용 없음 | 🟢 안전 |
| SNS | @{후보명} 계정 존재 | 🟡 주의 |
| 경쟁사 | AWS에서 유사명 사용 중 | 🔴 위험 |

리스크 레벨 기준:
- 🟢 안전: 동일/유사명 사용 없음
- 🟡 주의: 다른 업종에서 유사명 사용 (법무팀 확인 권장)
- 🔴 위험: 동일 업종 또는 주요 경쟁사에서 사용 중 (재검토 권장)

---

### 5단계: SharePoint 폴더 생성 + Word 초안 업로드

환경변수 확인:
- `OUTLOOK_CLIENT_ID`, `OUTLOOK_CLIENT_SECRET`: 없으면 Microsoft Graph API 연동 불가 안내
- `SHAREPOINT_SITE_URL`: 없으면 기본 경로 사용 또는 확인 요청

**폴더 경로**: `네이밍검토/{사업부}/{솔루션명}_{YYYYMMDD}/`

**파일명**: `{사업부}_{솔루션명}_네이밍검토_{YYYYMMDD}.docx`

Word 초안 섹션 구성 및 섹션 6 상세 스펙 → `references/word-template.md` 참조

동일 폴더 이미 존재 시 (`@microsoft.graph.conflictBehavior: fail` → 409):
> "{사업부}/{솔루션명}_{날짜}" 폴더가 이미 있어요. 덮어쓸까요?

---

### 6단계: Teams 링크 공유

`TEAMS_WEBHOOK_URL` 환경변수가 있으면 Teams 채널에 알림을 보내세요.

알림 메시지 형식:
```
📋 네이밍 검토 초안이 업로드되었습니다.
- 솔루션: {사업부} / {솔루션명}
- SharePoint: {폴더 링크}
- Word 편집: {공동편집 링크}
피드백을 댓글로 남겨주세요!
```

---

### 7단계: 완료 메시지 출력

```
{사업부} / {솔루션명} 네이밍 검토 완료!

📁 SharePoint: 네이밍검토/{사업부}/{솔루션명}_{날짜}/
📄 Word 초안: [Teams에서 열기 →]({링크})

**이름 후보:**
1. {후보1} — {설명}
2. {후보2} — {설명}
3. {후보3} — {설명}

🏛️ 상표권 조회 결과: (각 후보별 KIPRIS 링크 + 리스크)
🔎 SNS·경쟁사 검색 결과: (각 후보별 리스크 레벨)

**최종 추천:**
- 1순위: {후보명} — {브랜드 전략·핵심 가치 alignment 근거}
- 2순위: {후보명} — {근거}

**브랜드팀 의견 요약:**
- 경쟁 환경: {시장 포지셔닝 기회 1줄}
- 주요 경쟁사: {경쟁사1}, {경쟁사2}, {경쟁사3}
- 포지셔닝 제언: {차별화 포인트 1줄}

팀 피드백 완료 후 "{솔루션명} 완성본 배포해줘"라고 말씀해주세요!
```

---

### 8단계: 완성본 배포 (사용자 요청 시)

"{솔루션명} 완성본 배포해줘" 요청이 오면 실행하세요.

1. SharePoint에서 해당 Word 파일 최종본 확인
2. Teams 채널에 완성본 공지 (`TEAMS_WEBHOOK_URL`)
3. Outlook으로 이메일 발송

이메일 규칙 및 HTML 레이아웃 스펙 → `references/email-template.md` 참조

---

## 여러 솔루션 동시 처리

여러 솔루션 요청 시 각각 독립적으로 처리하되, 결과는 구분선(`---`)으로 분리하여 출력하세요.
각 솔루션은 별도 폴더(`{사업부}/{솔루션명}_{날짜}`)로 생성하고, 완성본 배포도 개별 트리거로 진행하세요.
기존 폴더가 있으면 즉시 409 감지 → 덮어쓰기 확인 메시지 출력 후 처리하세요.

---

## 오류 처리

| 상황 | 안내 메시지 |
|------|------------|
| Microsoft Graph 토큰 만료 | "인증이 만료됐어요. 다시 로그인해주세요." |
| SharePoint 권한 없음 | "SharePoint 폴더 생성 권한이 없어요. IT팀에 권한 요청해주세요." |
| 네이밍 가이드 파일 없음 | "naming architecture 폴더에 파일이 없어요. 자료를 먼저 넣어주세요." |
| SharePoint 성공 / Teams 실패 | SharePoint 링크는 제공, Teams 오류 원인 안내 |
| 동일 폴더 이미 존재 (409) | 덮어쓰기 확인 메시지 출력 → yes 시 `replace`, no 시 중단 |

SharePoint 업로드가 성공하면 Teams/이메일 실패 여부와 관계없이 링크는 항상 제공하세요.

---

## 참고 파일

- `references/word-template.md` — Word 초안 섹션 구성 + 섹션 6 상세 스펙
- `references/email-template.md` — 이메일 HTML 레이아웃 + 발송 규칙
- `references/review-history.md` — 지금까지의 네이밍 검토 이력 (AAEF, Q One, ToD™)
- `references/ingredient-brand-guide.md` — Ingredient Brand(Powered by X™) 검토 기준 + 적용 시점
