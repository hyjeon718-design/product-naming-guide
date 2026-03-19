> 📚 **참고 문서**: `/googleapis/google-api-python-client` (Context7)
> 공식 문서: https://github.com/googleapis/google-api-python-client
>
> ⚠️ **안내**: 이 가이드는 AI가 공식 문서를 참고하여 작성했으며, 정확하지 않을 수 있습니다.
> 설정하다가 막히면 Claude Code에게 "이 부분이 안 돼요"라고 물어보면서 진행하세요!
> Claude Code가 최신 문서를 다시 찾아서 도와드릴 거예요 😊

---

# Google Docs 연동 가이드

이 스킬은 Google Docs에 네이밍 검토 초안을 자동으로 생성합니다.

**예상 소요 시간**: 약 20-30분
**복잡도**: 중간 (OAuth 설정 필요)

---

## 필요한 환경변수

```
GOOGLE_CLIENT_ID=
GOOGLE_CLIENT_SECRET=
```

---

## 설정 단계

### 1단계: Google Cloud Console 접속

1. https://console.cloud.google.com 접속
2. Google 계정으로 로그인
3. 상단 프로젝트 선택 → **새 프로젝트** 클릭
4. 프로젝트 이름: `product-naming-guide` 입력 → **만들기**

### 2단계: Google Docs API 활성화

1. 왼쪽 메뉴 → **API 및 서비스** → **라이브러리**
2. 검색창에 `Google Docs API` 입력
3. **Google Docs API** 클릭 → **사용** 클릭
4. 같은 방법으로 `Google Drive API`도 활성화

### 3단계: OAuth 동의 화면 설정

1. 왼쪽 메뉴 → **API 및 서비스** → **OAuth 동의 화면**
2. User Type: **외부** 선택 → **만들기**
3. 앱 이름: `product-naming-guide` 입력
4. 지원 이메일: 본인 이메일 입력
5. **저장 후 계속** 반복 클릭 (나머지는 기본값)

### 4단계: 사용자 인증 정보 생성

1. 왼쪽 메뉴 → **API 및 서비스** → **사용자 인증 정보**
2. **+ 사용자 인증 정보 만들기** → **OAuth 클라이언트 ID**
3. 애플리케이션 유형: **데스크톱 앱** 선택
4. 이름: `naming-guide-client` 입력 → **만들기**
5. 팝업에서 **클라이언트 ID**와 **클라이언트 보안 비밀** 복사

### 5단계: 환경변수 설정

Claude Code에게 이렇게 말하세요:
```
구글 클라이언트 ID는 [복사한 ID]야, 시크릿은 [복사한 Secret]야
```

또는 `.env` 파일에 직접 입력:
```
GOOGLE_CLIENT_ID=복사한_클라이언트_ID
GOOGLE_CLIENT_SECRET=복사한_클라이언트_시크릿
```

---

## 처음 실행 시

스킬을 처음 실행하면 브라우저가 열리고 Google 로그인을 요청합니다.
로그인 후 권한을 허용하면 `token.json` 파일이 생성되고, 이후에는 자동으로 인증됩니다.

---

## 문제 해결

**"액세스 차단됨" 오류가 뜬다면**:
- OAuth 동의 화면에서 본인 이메일을 테스트 사용자로 추가하세요.
- API 및 서비스 → OAuth 동의 화면 → 테스트 사용자 → 이메일 추가

**토큰이 만료됐다면**:
- `token.json` 파일을 삭제하고 스킬을 다시 실행하면 재인증됩니다.
