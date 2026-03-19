# Microsoft Graph API 앱 등록 요청서

> **요청 부서**: 마케팅 / Brand & Impact Team
> **요청일**: 2026.03.19
> **요청자**: impact.brand@aiworkx.ai
> **목적**: 전사 브랜드 네이밍 협업 자동화 (사내 협업 툴 구축)

---

## 1. 요청 배경

마케팅팀에서 신규 제품·솔루션 네이밍 검토 업무를 자동화하기 위한 사내 협업 도구를 구축 중입니다.
현재 수작업으로 진행되는 아래 프로세스를 자동화하여 업무 효율을 높이고자 합니다.

**현재 프로세스 (수동)**
1. 네이밍 검토 Word 문서 작성
2. SharePoint에 수동 업로드
3. Teams에 링크 수동 공유
4. 피드백 수집 후 이메일 배포

**자동화 목표**
1. Claude Code 스킬 실행 → Word 검토 문서 자동 생성
2. SharePoint 지정 폴더에 자동 업로드
3. Teams 채널에 자동 알림 및 공동편집 링크 공유
4. 완성본 이메일 자동 배포

---

## 2. 요청 사항

**Azure Portal에서 앱 등록(App Registration) 1건 생성 요청드립니다.**

### 앱 기본 정보

| 항목 | 값 |
|------|-----|
| 앱 이름 | AIWORKX Naming Guide |
| 계정 유형 | 이 조직 디렉터리의 계정만 (단일 테넌트) |
| 리디렉션 URI | 없음 (또는 `http://localhost`) |
| 앱 유형 | Daemon / Background Service (사용자 상호작용 없음) |

### 필요한 API 권한 (Microsoft Graph)

| 권한 | 유형 | 용도 |
|------|------|------|
| `Files.ReadWrite.All` | Application | SharePoint 파일 업로드·조회 |
| `Sites.ReadWrite.All` | Application | SharePoint 사이트 접근 |
| `Mail.Send` | Application | Outlook 이메일 자동 발송 |
| `User.Read.All` | Application | 발신자 계정 확인 |

> ⚠️ 모두 **Application 권한** (위임 권한 아님) — 백그라운드 자동 실행용

### 관리자 동의 (Admin Consent)
- 위 권한 모두 **관리자 동의(Admin Consent) 필요**
- 등록 후 Azure Portal → Enterprise Applications → 해당 앱 → Permissions → **"Grant admin consent"** 클릭 요청

---

## 3. IT 관리자 설정 완료 후 전달 필요 정보

앱 등록 완료 시 아래 3가지 값을 마케팅팀(`impact.brand@aiworkx.ai`)으로 전달 부탁드립니다.

| 항목 | 위치 |
|------|------|
| **Application (Client) ID** | 앱 등록 → 개요 |
| **Directory (Tenant) ID** | 앱 등록 → 개요 |
| **Client Secret 값** | 앱 등록 → 인증서 및 암호 → 새 클라이언트 암호 생성 후 복사 |

> ⚠️ Client Secret은 생성 직후 1회만 확인 가능합니다. 반드시 즉시 복사하여 전달 부탁드립니다.

---

## 4. 보안 및 관리 기준

| 항목 | 내용 |
|------|------|
| 사용 범위 | 마케팅팀 전용 (Brand & Impact Team) |
| 접근 데이터 | SharePoint 마케팅 폴더, 마케팅팀 발신 이메일만 |
| 자격증명 보관 | 로컬 `.env` 파일 (Git 미포함, `.gitignore` 처리) |
| Secret 만료 | 1년 (만료 전 갱신 요청 예정) |
| 삭제 요청 시 | 요청 즉시 앱 등록 삭제 가능 |

---

## 5. SharePoint 사이트 URL 확인 요청

추가로, 마케팅팀 SharePoint 사이트 URL도 함께 확인 부탁드립니다.

> Teams → 마케팅 채널 → 파일 탭 → "SharePoint에서 열기" → 주소창 URL

예시: `https://aiworkx.sharepoint.com/sites/marketing`

---

## 6. 참고: 동일 자격증명으로 활용 가능한 기능

이번에 등록하는 앱 하나로 아래 기능을 모두 커버합니다.

- ✅ SharePoint 문서 자동 업로드
- ✅ Teams 파일 공유 링크 생성
- ✅ Outlook 이메일 자동 발송 (마케팅 배포)
- ✅ 향후 확장: 캘린더 일정 생성, Planner 태스크 연동

---

문의사항은 `impact.brand@aiworkx.ai` 또는 내선 마케팅팀으로 연락 부탁드립니다.

감사합니다.

**Brand & Impact Team**
AIWORKX
