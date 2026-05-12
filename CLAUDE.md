# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

---

## 스킬 개요

`product-naming-guide`는 AIWORKX 사업부/솔루션 네이밍 검토를 자동화하는 Claude Code 스킬이다.
스킬 정의 파일은 `SKILL.md` 하나이며, 실행 순서(0~8단계)가 모두 이 파일에 기술되어 있다.

---

## 핵심 파일

| 파일 | 역할 |
|------|------|
| `SKILL.md` | 스킬 실행 로직 전체 (트리거·단계별 지침·검토 이력) |
| `CLAUDE.md` | Claude Code 운영 지침 (이 파일) |
| `.claude/settings.json` | PostToolUse hook — SKILL.md 수정 시 자동 git push |
| `.env.example` | 필요한 환경변수 목록 |
| `연동가이드/` | SharePoint·Teams·Outlook 연동 가이드 |

---

## 환경변수

스킬 실행에 필요한 환경변수는 `.env.example`을 참고하여 `.env`에 설정한다.

| 변수 | 필수 | 용도 |
|------|------|------|
| `OUTLOOK_CLIENT_ID` | ✅ | Azure App Client ID (SharePoint·Outlook 공용) |
| `OUTLOOK_CLIENT_SECRET` | ✅ | Azure App Client Secret |
| `OUTLOOK_USER_EMAIL` | ✅ | 발신 이메일 |
| `DISTRIBUTION_EMAIL` | ✅ | 전사 배포 수신 이메일 |
| `SHAREPOINT_SITE_URL` | ✅ | SharePoint 사이트 URL |
| `TEAMS_WEBHOOK_URL` | 선택 | Teams Incoming Webhook |
| `KIPRIS_API_KEY` | 선택 | KIPRIS PLUS API (없으면 링크 방식 사용) |

---

## 네이밍 아키텍처 기준 파일 위치

`~/Documents/claude/projects/솔루션 네이밍 리뷰/` 폴더에 브랜드 아키텍처 기준 파일을 위치시켜야 한다.
- 지원 형식: `.pptx`, `.docx`, `.md`, `.pdf`
- 핵심 파일: `aiworkx_naming_architecture_master_diagram_l_0_l_6.md`, `AIWORKX_Brand_Governance.md`
- 파일이 없으면 스킬이 1단계에서 중단된다.

---

## SKILL.md 수정 시 자동 git push

`.claude/settings.json`에 PostToolUse hook이 설정되어 있다.
`SKILL.md`를 Edit/Write하면 자동으로 `git add → commit → push origin main`이 실행된다.
새 세션 시작 시 또는 `/hooks`를 한 번 열어야 hook이 활성화된다.

---

## 네이밍 추천 기준 (필수 준수)

- 네이밍 후보의 적합성은 **회사 브랜드 전략 및 핵심 가치(Core Value)와의 alignment** 여부로 판단한다.
- "CEO가 강조했다", "경영진 의견" 등 특정 인물 기반 표현 사용 **금지**.
- 대신 다음 표현을 사용한다:
  - "브랜드 전략 방향과 alignment"
  - "회사 핵심 가치(Core Value)에 부합"
  - "네이밍 아키텍처 원칙에 적합"
  - "사업 방향성과 일치"

---

## AIWORKX 브랜드 아키텍처 5대 Golden Rules

| Rule | 내용 |
|------|------|
| Rule 1 | 항상 AIWORKX로 시작. AWX 축약 외부 표기 금지 |
| Rule 2 | 카테고리 → 제품명 순서 (역전 불가) |
| Rule 3 | 카테고리는 4개만: **Test** (Verification 통합) / Agent / Data / Edu — 2026-05-12 Verification 카테고리 Test로 통합 |
| Rule 4 | 신규 카테고리는 NRB → 경영진 승인 필수 |
| Rule 5 | 해당 제품에 `Powered by ToD™` 표기 |

- **내부 표기**: `AIWORKX [Category] — [ProductName]`
- **외부 표기**: `AIWORKX [ProductName]`

---

## SharePoint 연동 정보

- **Site ID**: `testworks.sharepoint.com,3bc4c5d9-a42a-4591-8955-c1a696a252c6,3f646bda-c6d7-4ebe-9645-4dac22775110`
- **업로드 경로 패턴**: `네이밍검토/{사업부}/{솔루션명}_{YYYYMMDD}/`
- Microsoft Graph API — client credentials flow (tenant ID: `93014fae-b2c7-4069-aa55-a57ae1ab9ee1`)
- 파일 잠금(423) 발생 시: 다른 파일명으로 같은 폴더에 업로드 후 공유 링크 생성
