> 📚 **참고 문서**: `/microsoft/teams-sdk` (Context7)
> 공식 문서: https://github.com/microsoft/teams-sdk
>
> ⚠️ **안내**: 이 가이드는 AI가 공식 문서를 참고하여 작성했으며, 정확하지 않을 수 있습니다.
> 설정하다가 막히면 Claude Code에게 "이 부분이 안 돼요"라고 물어보면서 진행하세요!
> Claude Code가 최신 문서를 다시 찾아서 도와드릴 거예요 😊

---

# Microsoft Teams 연동 가이드

이 스킬은 완성된 네이밍 가이드 Word 파일을 Teams 채널에 자동으로 공유합니다.

**예상 소요 시간**: 약 15-20분
**복잡도**: 중간 (Incoming Webhook 설정)

---

## 필요한 환경변수

```
TEAMS_WEBHOOK_URL=
```

---

## 설정 단계

### 1단계: Teams 채널에서 Webhook 설정

1. Microsoft Teams 앱 열기
2. 파일을 공유할 **채널** 이동 (예: 마케팅팀, 브랜드전략 채널)
3. 채널 이름 옆 **...** (더보기) 클릭
4. **커넥터** 클릭

> ⚠️ **커넥터가 안 보인다면?**
> Teams 관리자가 커넥터를 비활성화했을 수 있어요.
> IT팀에 "Incoming Webhook 커넥터를 활성화해달라"고 요청하세요.

### 2단계: Incoming Webhook 생성

1. 커넥터 목록에서 **Incoming Webhook** 찾기
2. **구성** 클릭
3. Webhook 이름: `Naming Guide Bot` 입력
4. (선택) 아이콘 업로드
5. **만들기** 클릭
6. 생성된 **URL 전체 복사** (https://...webhook.office.com/... 형태)

### 3단계: 환경변수 설정

Claude Code에게 이렇게 말하세요:
```
Teams 웹훅 URL은 [복사한 URL]야
```

또는 `.env` 파일에 직접 입력:
```
TEAMS_WEBHOOK_URL=복사한_Webhook_URL
```

---

## 테스트

설정 후 Claude Code에게 "Teams 테스트 메시지 보내줘"라고 하면 연동이 잘 됐는지 확인할 수 있어요.

---

## 문제 해결

**메시지가 안 온다면**:
- Webhook URL이 올바른지 확인하세요 (URL이 길어요, 잘 복사됐는지 확인)
- 채널에 권한이 있는지 확인하세요

**"커넥터가 비활성화됨" 메시지**:
- Teams 관리자에게 해당 채널에서 Incoming Webhook 허용을 요청하세요
