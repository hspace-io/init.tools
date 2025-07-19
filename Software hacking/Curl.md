---
tags:
  - mac
  - windows
  - linux
  - web
  - debugging
  - application
---
## 설명
---
`curl`은 Command Line 기반으로 다양한 프로토콜을 사용하여 데이터를 전송할 수 있는 도구입니다. 주로 웹 개발, API 테스트, 데이터 다운로드 등 다양한 작업에 활용됩니다.

## 설치 영역
---
### Windows
`C:\Windows\System32\curl.exe` (Windows 10 1803 이상)

### mac
`/usr/bin/curl`

### linux
`/usr/bin/curl`

## 주요 기능
---
- 웹 서버에서 데이터 가져오기 (GET 요청)
- 웹 서버로 데이터 보내기 (POST, PUT, DELETE 등 요청)
- API 테스트 및 디버깅
- 파일 다운로드 및 업로드
- HTTP 헤더 확인 및 설정
- 웹 스크래핑 (제한적)

## 설치 방법
---
### Windows
- Windows 10 이후 내장 되어 사용 가능합니다.

1. 설치 필요 시 [curl 공식 웹사이트](https://curl.se/windows/)에서 압축 파일을 다운 받아 압축해제를 합니다.
2. 원하는 디렉토리로 `curl.exe`를 옮기고, 해당 디렉토리를 시스템 `PATH`에 등록하여 사용할 수 있습니다.
### mac
- 기본 설치 되어 있습니다.
- 설치 필요시 아래 명령어를 터미널에 입력하시면 됩니다.
```sh
brew install curl
```

### linux
- 배포판에 따라 다르나 대부분 기본 설치되어 있습니다.
- 설치 필요 시 아래 명령어를 터미널에 입력하면 됩니다.
```sh
sudo apt install curl
```

## 간단 가이드
---
1.  **기본 GET 요청**
    ```sh
    # example.com의 HTML 내용을 가져옴
    curl https://example.com
    ```

2.  **헤더 정보와 함께 보기 (-v)**
    ```sh
    # 요청 및 응답 헤더를 자세히 출력
    curl -v https://example.com
    ```

3.  **응답 헤더만 보기 (-I)**
    ```sh
    # HTTP 응답 헤더만 확인
    curl -I https://example.com
    ```

4.  **파일로 저장 (-o, -O)**
    ```sh
    # 결과를 output.html 파일로 저장
    curl -o output.html https://example.com

    # 원격 파일 이름 그대로 저장 (예: download.zip)
    curl -O https://example.com/download.zip
    ```

5.  **POST 요청 보내기 (-X POST, -d)**
    ```sh
    # 폼 데이터 전송
    curl -X POST -d "name=test&email=test@example.com" https://api.example.com/users

    # JSON 데이터 전송
    curl -X POST -H "Content-Type: application/json" -d '{"key":"value"}' https://api.example.com/data
    ```

6.  **사용자 정의 헤더 추가 (-H)**
    ```sh
    # 인증 토큰을 헤더에 추가하여 요청
    curl -H "Authorization: Bearer YOUR_TOKEN" https://api.example.com/secure-data
    ```

7.  **리다이렉트 따라가기 (-L)**
    ```sh
    # HTTP 301/302 리다이렉트가 발생하면 최종 목적지까지 따라감
    curl -L http://google.com
    ```

- SSL/TLS 인증서: HTTPS를 통해 데이터를 전송할 때, cURL은 신뢰할 수 있는 인증 기관(CA)의 인증서를 사용하여 서버의 유효성을 검사합니다. 만약 서버가 자체 서명된 인증서를 사용하거나, cURL이 인식하지 못하는 CA의 인증서를 사용하는 경우, `-k` 또는 `--insecure` 옵션을 사용하여 인증서 검사를 비활성화할 수 있습니다. **하지만 `-k` 또는 `--insecure` 옵션은 보안 위험을 초래할 수 있으므로, 프로덕션 환경에서는 사용하지 않는 것이 좋습니다.** 가능하면 올바른 CA 인증서를 설치하거나, 서버에서 신뢰할 수 있는 CA의 인증서를 사용하도록 구성하는 것이 좋습니다.

## 관련 URL
---
[curl 공식 웹사이트](https://curl.se/windows/)

