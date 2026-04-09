# 이메일 HTML 레이아웃 스펙

## 필수 규칙
- **수신자**: `Impact.brand@aiworkx.ai` 단독 (다른 주소 절대 금지)
- **saveToSentItems**: `true` (발송 이력 추적용)
- **제목 형식**: `[AIWORKX] {솔루션명} 네이밍검토 {버전} — {부제}`
- **이메일 발송 가드**: SKILL.md의 "이메일 발송 가드 규칙" 반드시 준수 (업로드 성공 확인 후에만 발송)

## HTML 템플릿

아래 HTML을 기반으로 `{변수}`를 치환하여 사용합니다.
색상·구조는 반드시 이 스펙을 따르세요.

```html
<div style="max-width:640px;margin:0 auto;font-family:'Segoe UI',Arial,sans-serif;color:#222;">

  <!-- ========== 헤더 바 ========== -->
  <div style="background:#1a1a1a;padding:20px 28px;border-radius:8px 8px 0 0;display:flex;align-items:center;justify-content:space-between;">
    <span style="color:#fff;font-size:18px;font-weight:bold;">AIWORKX 브랜드팀</span>
    <span style="background:#333;color:#ccc;font-size:12px;padding:4px 10px;border-radius:4px;">{BADGE_TEXT}</span>
  </div>
  <!-- BADGE_TEXT 예: "ToD™ Naming Review v4-1", "AAEF Naming Review v4-1" -->

  <!-- ========== 본문 영역 ========== -->
  <div style="background:#fff;padding:28px;border:1px solid #e0e0e0;border-top:none;">

    <!-- 제목 + 날짜 -->
    <h1 style="font-size:22px;color:#111;margin:0 0 4px 0;">{EMAIL_TITLE}</h1>
    <p style="color:#888;font-size:13px;margin:0 0 20px 0;">{DATE}</p>

    <!-- 인사말 + 소개 -->
    <p style="font-size:14px;line-height:1.6;">안녕하세요, AIWORKX 브랜드팀입니다.</p>
    <p style="font-size:14px;line-height:1.6;">{INTRO_TEXT}</p>

    <!-- ========== 1순위 후보 하이라이트 박스 ========== -->
    <div style="background:#f5f5f5;border:1px solid #e0e0e0;border-radius:6px;padding:20px;margin:20px 0;">
      <p style="font-size:12px;color:#666;margin:0 0 8px 0;">★ 1순위 후보</p>
      <h2 style="font-size:28px;font-weight:bold;margin:0 0 8px 0;">{TOP1_NAME}</h2>
      <p style="font-size:13px;color:#666;margin:0 0 16px 0;">{TOP1_SUBTITLE}</p>
      <!-- 속성 테이블 (선택) -->
      <table style="width:100%;font-size:13px;border-collapse:collapse;">
        <tr>
          <td style="color:#888;padding:4px 0;width:100px;vertical-align:top;">{ATTR1_LABEL}</td>
          <td style="padding:4px 0;">{ATTR1_VALUE}</td>
        </tr>
        <tr>
          <td style="color:#888;padding:4px 0;vertical-align:top;">{ATTR2_LABEL}</td>
          <td style="padding:4px 0;">{ATTR2_VALUE}</td>
        </tr>
      </table>
    </div>

    <!-- ========== 주요 변경/업데이트 사유 박스 (노란색) ========== -->
    <div style="background:#FFF9E6;border-left:4px solid #F5C518;padding:14px 16px;margin:16px 0;border-radius:0 4px 4px 0;">
      <p style="font-size:13px;font-weight:bold;margin:0 0 6px 0;">{HIGHLIGHT_TITLE}</p>
      <p style="font-size:13px;margin:0;line-height:1.5;">{HIGHLIGHT_BODY}</p>
    </div>

    <!-- ========== 전체 후보 현황 테이블 ========== -->
    <h3 style="font-size:15px;margin:24px 0 12px 0;">{TABLE_TITLE}</h3>
    <table style="width:100%;border-collapse:collapse;font-size:13px;">
      <thead>
        <tr style="background:#2a2a2a;color:#fff;">
          <th style="padding:10px 12px;text-align:left;border:1px solid #444;">순위</th>
          <th style="padding:10px 12px;text-align:left;border:1px solid #444;">후보</th>
          <th style="padding:10px 12px;text-align:left;border:1px solid #444;">발음</th>
          <th style="padding:10px 12px;text-align:left;border:1px solid #444;">TM 리스크</th>
        </tr>
      </thead>
      <tbody>
        <!-- 1순위 행: 굵게 -->
        <tr style="background:#fff;">
          <td style="padding:10px 12px;border:1px solid #e0e0e0;font-weight:bold;">★ 1순위</td>
          <td style="padding:10px 12px;border:1px solid #e0e0e0;font-weight:bold;">{ROW1_NAME}</td>
          <td style="padding:10px 12px;border:1px solid #e0e0e0;">{ROW1_PRON}</td>
          <td style="padding:10px 12px;border:1px solid #e0e0e0;">{ROW1_TM}</td>
        </tr>
        <!-- 2순위~ 행: 교대 배경 -->
        <tr style="background:#fafafa;">
          <td style="padding:10px 12px;border:1px solid #e0e0e0;">2순위</td>
          <td style="padding:10px 12px;border:1px solid #e0e0e0;">{ROW2_NAME}</td>
          <td style="padding:10px 12px;border:1px solid #e0e0e0;">{ROW2_PRON}</td>
          <td style="padding:10px 12px;border:1px solid #e0e0e0;">{ROW2_TM}</td>
        </tr>
        <!-- 필요한 만큼 행 추가 -->
      </tbody>
    </table>

    <!-- ========== 경고/주의 박스 (선택, 노란색) ========== -->
    <div style="background:#FFF9E6;border-left:4px solid #F5C518;padding:14px 16px;margin:20px 0;border-radius:0 4px 4px 0;">
      <p style="font-size:13px;font-weight:bold;margin:0 0 6px 0;">⚠️ {WARNING_TITLE}</p>
      <p style="font-size:13px;margin:0;line-height:1.5;">{WARNING_BODY}</p>
    </div>

    <!-- ========== SharePoint 링크 ========== -->
    <div style="margin:24px 0 16px 0;">
      <p style="font-size:13px;color:#888;margin:0 0 4px 0;">📎 SharePoint: {SP_FOLDER_PATH}</p>
      <p style="font-size:13px;margin:0;">📄 문서: <a href="{SP_DOC_URL}" style="color:#2E75B6;">{SP_DOC_FILENAME}</a></p>
    </div>

  </div>

  <!-- ========== 푸터 ========== -->
  <div style="background:#f5f5f5;padding:14px 28px;border:1px solid #e0e0e0;border-top:none;border-radius:0 0 8px 8px;">
    <p style="font-size:12px;color:#888;margin:0;">AIWORKX 브랜드팀 | <a href="mailto:impact.brand@aiworkx.ai" style="color:#2E75B6;">impact.brand@aiworkx.ai</a></p>
  </div>

</div>
```

## 변수 설명

| 변수 | 필수 | 설명 | 예시 |
|------|------|------|------|
| `{BADGE_TEXT}` | ✅ | 헤더 오른쪽 뱃지 | `ToD™ Naming Review v4-1` |
| `{EMAIL_TITLE}` | ✅ | 본문 대제목 | `ToD™ 대안 네이밍 — AXDC™ 1순위 승격 (v3 rev.3)` |
| `{DATE}` | ✅ | 날짜 | `2026년 4월 9일` |
| `{INTRO_TEXT}` | ✅ | 소개 1~2줄 | `ToD™ 대안 네이밍 검토에서 AXDC™가 1순위로 승격되었습니다.` |
| `{TOP1_NAME}` | ✅ | 1순위 후보명 (큰 글씨) | `AXDC™` |
| `{TOP1_SUBTITLE}` | ✅ | 1순위 부가 설명 | `Powered by AXDC™ \| /악-디씨/ \| 3음절` |
| `{ATTR1_LABEL}` | 선택 | 속성 라벨1 | `기술 레이어` |
| `{ATTR1_VALUE}` | 선택 | 속성 값1 | `AX(AI eXecution) + DC(Direct Compute)` |
| `{ATTR2_LABEL}` | 선택 | 속성 라벨2 | `브랜드 레이어` |
| `{ATTR2_VALUE}` | 선택 | 속성 값2 | `AC/DC 변환 — 두 힘의 공존 메타포` |
| `{HIGHLIGHT_TITLE}` | 선택 | 노란 박스 제목 | `순위 변경 사유` |
| `{HIGHLIGHT_BODY}` | 선택 | 노란 박스 본문 | `AXDC™의 AC/DC 이중 레이어 의미...` |
| `{TABLE_TITLE}` | ✅ | 테이블 제목 | `v4-1 전체 후보 현황` |
| `{ROWn_NAME}` | ✅ | 후보명 | `AxDC™` |
| `{ROWn_PRON}` | ✅ | 발음 | `/에이엑스디씨/` |
| `{ROWn_TM}` | ✅ | TM 리스크 | `🟢 KIPRIS 0건` |
| `{WARNING_TITLE}` | 선택 | 경고 박스 제목 | `법무팀 확인 필요` |
| `{WARNING_BODY}` | 선택 | 경고 박스 본문 | `AXDC™ KIPRIS Class 42 정식 조회...` |
| `{SP_FOLDER_PATH}` | ✅ | SharePoint 폴더 경로 | `네이밍 검토/기타/ToD_20260409_v4/` |
| `{SP_DOC_URL}` | ✅ | SharePoint 공유 링크 | `https://testworks.sharepoint.com/...` |
| `{SP_DOC_FILENAME}` | ✅ | 파일명 | `기타_ToD_네이밍검토_20260409_v4-1.docx` |

## 디자인 가이드라인

| 요소 | 스펙 |
|------|------|
| 전체 너비 | max-width: 640px, 중앙 정렬 |
| 헤더 바 | 배경 `#1a1a1a` (검정), 흰색 텍스트, 뱃지는 `#333` 배경 |
| 1순위 하이라이트 | 배경 `#f5f5f5`, 테두리 `#e0e0e0`, 둥근 모서리 |
| 노란 박스 (업데이트/경고) | 배경 `#FFF9E6`, 왼쪽 보더 `#F5C518` 4px |
| 테이블 헤더 | 배경 `#2a2a2a`, 흰색 텍스트 |
| 테이블 본문 | 교대 배경 `#fff` / `#fafafa` |
| 링크 색상 | `#2E75B6` |
| 푸터 | 배경 `#f5f5f5`, 12px, 회색 텍스트 |
| 폰트 | `'Segoe UI', Arial, sans-serif` |
| TM 아이콘 | 🟢 클린 / 🟡 주의 / 🔴 위험 |

## 선택적 섹션

모든 `선택` 변수 블록은 해당 내용이 없으면 HTML에서 해당 `<div>` 자체를 제거합니다.
- 속성 테이블 (`{ATTR*}`) — 1순위 후보에 기술/브랜드 레이어 설명이 있을 때만
- 노란 박스 (`{HIGHLIGHT_*}`) — 순위 변경, 주요 업데이트 사유가 있을 때만
- 경고 박스 (`{WARNING_*}`) — 법무팀 확인, TM 리스크 등 주의사항이 있을 때만
