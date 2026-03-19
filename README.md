# product-naming-guide

> Claude Code 스킬 — 사업부/솔루션별 네이밍 검토 자동화

사업부명과 솔루션명을 입력하면 브랜드 아키텍처 기준으로 이름 후보를 생성하고,
상표권 조회 · SNS/Google 유사 브랜드 검색 · 경쟁사 검색까지 자동으로 수행합니다.
검토 결과는 SharePoint에 Word 초안으로 저장되고, Teams 및 이메일로 배포됩니다.

## 주요 기능

- 네이밍 아키텍처 가이드 기반 이름 후보 3~5개 생성
- 특허청 KIPRIS 상표권 간단 조회 링크 자동 생성 + WebSearch 유사 상표 확인
- Google · LinkedIn · X(Twitter) · Instagram SNS 유사 브랜드명 검색
- Microsoft · Google · AWS · Salesforce 등 경쟁사 제품명 중복 검색
- SharePoint 사업부별 폴더 자동 생성 + Word 초안 업로드
- Microsoft Teams 공동편집 링크 공유
- Outlook 이메일 전사 배포

## 사용법

```
/product-naming-guide
```

또는 자연어로:

```
Test사업부 Q-one 네이밍 검토해줘
```

```
AAEF 솔루션 이름 추천해줘, 사업부는 Test야
```

완성 후 배포:

```
Q-one 완성본 배포해줘
```

## 설치

### 1. 이 레포를 클론

```bash
git clone https://github.com/hyjeon718-design/product-naming-guide.git
cd product-naming-guide
```

### 2. 스킬 등록

Claude Code 설정 파일에 스킬 경로를 추가하세요.

### 3. 환경변수 설정

`.env.example`을 복사하여 `.env` 파일을 만들고 값을 채워주세요:

```bash
cp .env.example .env
```

| 변수명 | 설명 | 필수 여부 |
|--------|------|----------|
| `OUTLOOK_CLIENT_ID` | Azure App Client ID (SharePoint + Outlook 공통) | 필수 |
| `OUTLOOK_CLIENT_SECRET` | Azure App Client Secret | 필수 |
| `OUTLOOK_USER_EMAIL` | 발신 이메일 주소 | 필수 |
| `DISTRIBUTION_EMAIL` | 전사 배포 수신 이메일 | 필수 |
| `SHAREPOINT_SITE_URL` | SharePoint 사이트 URL | 필수 |
| `TEAMS_WEBHOOK_URL` | Teams Incoming Webhook URL | 선택 |
| `KIPRIS_API_KEY` | KIPRIS PLUS API 키 (없으면 링크 방식 사용) | 선택 |

### 4. Microsoft Graph API 설정

SharePoint + Teams + Outlook 연동을 위해 Azure App 등록이 필요합니다.

- [📘 SharePoint + Outlook 설정 가이드](연동가이드/outlook-email.md)
- [📘 Teams 설정 가이드](연동가이드/microsoft-teams.md)
- [📋 IT관리자 API 요청서](연동가이드/IT관리자_API요청서.md)

### 5. 네이밍 아키텍처 가이드 준비

`~/Documents/naming architecture/` 폴더에 브랜드 아키텍처 기준 파일을 넣어주세요.
(`.pptx`, `.docx`, `.md`, `.pdf` 형식 지원)

## 워크플로우

```
사업부+솔루션 입력
  → 네이밍 후보 생성
  → 상표권 간단 조회 (KIPRIS)
  → SNS · Google · 경쟁사 유사 브랜드 검색
  → SharePoint 폴더 생성 + Word 초안 업로드
  → Teams 공동편집 링크 공유
  → [팀 피드백]
  → 완성본 Teams 공지 + 이메일 전사 배포
```

## 파일 구조

```
product-naming-guide/
├── SKILL.md                  # 스킬 정의
├── .env.example              # 환경변수 예시
├── .gitignore
└── 연동가이드/
    ├── microsoft-teams.md    # Teams 설정 가이드
    ├── outlook-email.md      # SharePoint + Outlook 설정 가이드
    └── IT관리자_API요청서.md  # IT팀 권한 요청 양식
```
