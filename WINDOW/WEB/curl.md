# window-CURL

## 설명
cURL은 Command Line 기반으로 다양한 프로토콜을 사용하여 데이터를 전송할 수 있는 도구입니다.  Windows-CURL은 cURL을 Windows 환경에서 사용할 수 있도록 제공하는 버전입니다. 주로 웹 개발, API 테스트, 데이터 다운로드 등 다양한 작업에 활용됩니다.

## 설치 영역
`C:\Program Files\cURL\bin` (기본 설치 경로, 설치 시 변경 가능)

## 사용처
- 웹 서버에서 데이터 가져오기 (GET 요청)
- 웹 서버로 데이터 보내기 (POST, PUT, DELETE 등 요청)
- API 테스트 및 디버깅
- 파일 다운로드 및 업로드
- HTTP 헤더 확인 및 조작
- 웹 스크래핑 (제한적)

## 설치(접속) 방법
1. **cURL 다운로드:**  [cURL 공식 웹사이트](https://curl.se/download.html) 에서 Windows용 바이너리 파일을 다운로드합니다.  "Win64 - Generic" 또는 "Win32 - Generic" 섹션에서 "curl" 이라고 표시된  ZIP 파일을 선택합니다. (시스템 아키텍처에 맞는 버전을 선택하세요 - 32bit or 64bit).
2. **압축 해제:** 다운로드한 ZIP 파일의 압축을 원하는 위치에 풉니다. (예: `C:\curl`)
3. **환경 변수 설정 (선택 사항이지만 권장):**
    *   Windows 검색창에 "환경 변수"를 입력하고 "시스템 환경 변수 편집"을 선택합니다.
    *   "시스템 변수" 섹션에서 "Path" 변수를 선택하고 "편집"을 클릭합니다.
    *   "새로 만들기"를 클릭하고 cURL 실행 파일(`curl.exe`)이 있는 폴더의 경로를 추가합니다 (예: `C:\curl\bin`).  압축을 푼 폴더 안에 `bin` 폴더가 있다면 그 경로를 사용하고, 없다면 `curl.exe`가 있는 폴더의 경로를 사용합니다.
    *   "확인"을 눌러 모든 창을 닫습니다.
4. **확인:**  명령 프롬프트(cmd) 또는 PowerShell을 열고 `curl --version` 명령을 실행합니다.  cURL 버전 정보가 표시되면 설치가 성공적으로 완료된 것입니다.

## 접속 화면
![명령 프롬프트에서 curl --version 실행 결과](curl_version_example.png)


## 주의 사항
- **Windows Defender 또는 방화벽:**  Windows Defender 또는 기타 방화벽 소프트웨어가 cURL의 네트워크 연결을 차단할 수 있습니다.  필요한 경우 예외 규칙을 추가해야 할 수 있습니다.
- **SSL/TLS 인증서:**  HTTPS를 통해 데이터를 전송할 때, cURL은 신뢰할 수 있는 인증 기관(CA)의 인증서를 사용하여 서버의 유효성을 검사합니다.  만약 서버가 자체 서명된 인증서를 사용하거나,  cURL이 인식하지 못하는 CA의 인증서를 사용하는 경우, `-k` 또는 `--insecure` 옵션을 사용하여 인증서 검사를 비활성화할 수 있습니다.  **하지만 `-k` 또는 `--insecure` 옵션은 보안 위험을 초래할 수 있으므로,  프로덕션 환경에서는 사용하지 않는 것이 좋습니다.**  가능하면 올바른 CA 인증서를 설치하거나, 서버에서 신뢰할 수 있는 CA의 인증서를 사용하도록 구성하는 것이 좋습니다.


## 관련 URL
-   **cURL 공식 웹사이트:** [https://curl.se/](https://curl.se/)
-   **cURL 메뉴얼 페이지:** [https://curl.se/docs/manpage.html](https://curl.se/docs/manpage.html)
-   **cURL 튜토리얼:** [https://curl.se/docs/tutorial.html](https://curl.se/docs/tutorial.html)
-   **Everything curl (cURL에 대한 상세한 가이드):** [https://everything.curl.dev/](https://everything.curl.dev/)
