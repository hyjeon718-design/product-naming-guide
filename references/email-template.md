# 이메일 HTML 레이아웃 스펙

## 필수 규칙
- **수신자**: `Impact.brand@aiworkx.ai` 단독 (다른 주소 절대 금지)
- **중복 방지**: `saveToSentItems: false` 반드시 설정 (true 시 Exchange에서 2회 전달 발생)
- **제목**: `[네이밍 검토] AIWORKX {사업부} — {솔루션명} 네이밍 후보 검토 초안`
- **Word 파일 첨부** 필수 — 누락 시 발송 금지

## Word 파일 첨부 방법 (Microsoft Graph API)

SharePoint에서 파일을 가져와 base64로 인코딩 후 attachments 배열에 포함:

```json
{
  "message": {
    "attachments": [
      {
        "@odata.type": "#microsoft.graph.fileAttachment",
        "name": "{사업부}_{솔루션명}_네이밍검토_{YYYYMMDD}.docx",
        "contentType": "application/vnd.openxmlformats-officedocument.wordprocessingml.document",
        "contentBytes": "{base64_encoded_file_content}"
      }
    ]
  }
}
```

파일 다운로드 → base64 인코딩 순서:
1. Graph API로 파일 bytes 가져오기:
   `GET /sites/{site-id}/drive/root:/{경로}/{파일명}.docx:/content`
2. 응답 bytes를 base64 인코딩
3. 위 attachments 구조에 삽입 후 sendMail 호출

## HTML 레이아웃

```
헤더 (배경 #1F3E7A):
  - 흰색 대제목: "AIWORKX 네이밍 검토 초안"
  - 연파랑 소제목: "AIWORKX {사업부} — {솔루션명} | {날짜}"

본문:
  - 인사: "Brand & Impact Team,"
  - 설명 1~2줄: 솔루션명, 핵심 기능, 후보 개수

요약 테이블 (3행):
  | 최종 추천 | ① {1순위} | ② {2순위} |
  | 탈락      | {탈락 후보} (사유)         |
  | 다음 단계 | 팀 피드백 → NRB 상정 → 경영진 최종 승인 |

CTA 버튼 (배경 #1F3E7A): "📄 Word 초안 Teams에서 열기 →" → SharePoint 링크
푸터: SharePoint 경로 + "Powered by ToD™ · AIWORKX Brand & Impact Team"
```
