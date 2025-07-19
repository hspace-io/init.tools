---
tags:
  - linux
  - windows
  - mac
  - webapp
  - api_testing
  - automation
  - application
  - multi_platform
---
## 설명
---
`Postman`은 API 개발, 테스트, 문서화, 자동화에 특화된 오픈소스 기반의 통합 플랫폼입니다. 직관적인 GUI 환경에서 HTTP 요청을 쉽게 생성/전송하고, 응답을 분석하며, 다양한 테스트와 자동화, 협업 기능 등을 제공하는 도구입니다.

## 설치 영역
---
### Windows
`C:\Users\<사용자 이름>\AppData\Local\Postman` (기본 설치 경로)

### mac
`/Applications/Postman.app`

### Linux
`/opt/Postman` (설치 방식에 따라 다름)

## 주요 기능
---
- `HTTP 요청 지원`: GET, POST, PUT, DELETE 등 RESTfull API 지원
- `Collections`: 요청들을논리적으로 그룹화해 관리 및 재사용
- `환경 변수/글로벌 변수`: 환경별로 변수 관리, API 키·토큰 등 반복 데이터 전환
- `Collection Runner`: 요청을 순차적으로 실행, 반복 테스트 및 데이터 생성, 응답 검증, 변수 저장 등 자동화
- `Pre-request Script & Test Script`: 요청 전/후 Java Script로 동적 데이터 생성, 응답 검증, 변수 저장 등 자동화
- `API 문서화`: 요청/응답 예시, 설명 등 자동 문서화 및 공유
- `다양한 인증 지원`: 다양한 인증 방식 내장 (Basic, API Key, OAuth 1.0/2.0, Bearer Token 등)
- `테스트 및 어설션`: 응답 코드, 바디, 헤더 등 조건 검증 가능

## 설치 방법
---
### Windows
1. [Postman 공식 웹사이트](https://www.postman.com/)에서 환경에 맞는 설치 파일을 다운받습니다.
2. 설치 파일을 실행시켜 설치를 진행합니다.

### Linux (x64)
- 아래 명령어를 터미널에 입력하여 CLI 버전을 설치합니다.
```sh
curl -o- "https://dl-cli.pstmn.io/install/osx_64.sh" | sh
```

### mac
- 아래 명령어를 터미널에 입력하여 설치합니다.
```sh
brew install --cask postman
```


## 간단 가이드
---
1.  **새 요청 생성**: Postman을 실행하고 `+` 버튼을 클릭하여 새 HTTP 요청 탭을 엽니다.

2.  **요청 설정**: 
    *   **메서드 선택**: GET, POST, PUT, DELETE 등 HTTP 메서드를 선택합니다.
    *   **URL 입력**: 요청을 보낼 API 엔드포인트 URL을 입력합니다.
    *   **헤더/바디 설정**: `Headers` 탭에서 필요한 헤더를 추가하고, `Body` 탭에서 요청 본문(JSON, Form Data 등)을 설정합니다.

3.  **요청 전송**: `Send` 버튼을 클릭하여 요청을 보냅니다.

4.  **응답 확인**: 요청이 성공적으로 전송되면 하단에 서버로부터의 응답이 표시됩니다. `Body`, `Headers`, `Test Results` 탭에서 응답 내용을 분석할 수 있습니다.

5.  **컬렉션 저장**: `Save` 버튼을 클릭하여 현재 요청을 컬렉션에 저장합니다. 컬렉션은 요청들을 그룹화하고 관리하는 데 사용됩니다.

6.  **환경 변수 사용**: `Environments` 드롭다운 메뉴에서 환경을 선택하거나 새로 생성하여, API 키나 기본 URL과 같은 변수를 관리할 수 있습니다. 요청 URL이나 헤더 등에서 `{{variable_name}}` 형식으로 변수를 사용할 수 있습니다.

7.  **테스트 스크립트 작성**: `Tests` 탭에서 JavaScript 코드를 작성하여 응답을 검증하고 테스트 결과를 확인할 수 있습니다. (예: `pm.test("Status code is 200", function () { pm.response.to.have.status(200); });`)

## 관련 URL
---
[Postman 공식 웹사이트](https://www.postman.com/)
[Postman Learning Center](https://learning.postman.com/)
