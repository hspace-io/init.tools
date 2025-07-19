---
tags:
  - mac
  - windows
  - linux
  - web
  - webapp
  - debugging
  - application
  - web_security
---
## 설명
---
`Burp Suite`는 웹 애플리케이션 보안 테스트를 위한 통합 도구입니다. 웹사이트의 취약점을 분석하고 공격 시나리오를 시뮬레이션할 때 주로 사용됩니다.

## 설치 영역
---
### mac
`/Applications/Burp Suite.app`

## 주요 기능
---
- `Proxy`: 사용자의 웹 브라우저와 서버 사이의 트래픽을 가로채고 수정 할 수 있음
- `Scanner`: 자동으로 웹 애플리케이션의 취약점을 탐지 (Professional 버전 이상에서 제공)
- `Intercepter`: HTTP 요청/응답을 실시간으로 수정 가능
- `Repeater`: 같은 요청을 반복해서 보내며 수동 테스트 수행
- `Intruder`: 자동화된 공격 (예: 로그인 크래킹, SQL 인젝션 시동 등) 가능
- `Sequencer`: 세션 토큰의 예측 가능성을 분석

## 설치 방법
---
### Windows
#### 설치 파일을 이용하여 설치
1. [PortSwigger 웹사이트](https://portswigger.net/burp/communitydownload)에서 Burp Suite Community Edition(무료 버전)을 다운로드 합니다.
2. 다운로드한 설치 파일을 실행하여 설치합니다.

### mac
#### 설치 파일을 이용하여 설치
1. [PortSwigger 웹사이트](https://portswigger.net/burp/communitydownload)에서 Burp Suite Community Edition(무료 버전)을 다운로드 합니다.
2. 다운로드한 설치 파일을 실행하여 설치합니다.
#### homebrew를 이용하여 설치
1. 아래의 명령어를 터미널에 입력하여 설치합니다.
```sh
brew install --cask burp-bsuite
```

## 간단 가이드
---
1.  **프록시 및 인증서 설정**
    *   **프록시 설정**: Burp Suite는 기본적으로 로컬 프록시(`127.0.0.1:8080`)를 사용합니다. 웹 브라우저의 프록시 설정을 이 주소로 변경해야 합니다.
        *   `Firefox`: 설정 > 일반 > 네트워크 설정 > 설정... > 수동 프록시 구성 (HTTP 프록시: 127.0.0.1, 포트: 8080, "이 프록시 설정을 HTTPS에도 사용" 체크)
        *   `Chrome`: FoxyProxy와 같은 확장 프로그램을 사용하면 편리하게 프록시를 켜고 끌 수 있습니다.
    *   **인증서 설치**: HTTPS 트래픽을 분석하려면 Burp Suite의 CA 인증서를 브라우저에 설치해야 합니다.
        1.  Burp Suite가 실행된 상태에서 브라우저로 `http://burp` 또는 `http://127.0.0.1:8080`에 접속합니다.
        2.  `CA Certificate` 버튼을 클릭하여 인증서(`cacert.der`)를 다운로드합니다.
        3.  브라우저의 인증서 관리자에서 다운로드한 인증서를 "신뢰할 수 있는 루트 인증 기관"으로 가져옵니다.

2.  **트래픽 가로채기 (Intercept)**
    *   Burp Suite의 `Proxy` 탭 > `Intercept` 탭으로 이동합니다.
    *   `Intercept is on` 버튼이 활성화되어 있는지 확인합니다.
    *   브라우저에서 웹사이트에 접속하면, 해당 HTTP 요청이 Burp Suite에 잡히게 됩니다.
    *   `Forward` 버튼을 눌러 요청을 서버로 보내거나, `Drop` 버튼으로 요청을 버릴 수 있습니다.
    *   요청/응답 내용을 직접 수정하여 서버나 브라우저로 보낼 수도 있습니다.

3.  **요청 재전송 (Repeater)**
    *   `Proxy` > `HTTP history` 탭에서 분석하고 싶은 요청을 마우스 오른쪽 버튼으로 클릭하고 `Send to Repeater`를 선택합니다.
    *   `Repeater` 탭으로 이동하면 해당 요청이 로드되어 있습니다.
    *   요청의 파라미터나 헤더를 수정한 후 `Send` 버튼을 누르면 서버의 응답을 즉시 확인할 수 있어, 취약점 분석에 매우 유용합니다.

4.  **자동화 공격 (Intruder)** - Community 버전에서는 속도 제한이 있음
    *   `Proxy` > `HTTP history` 탭에서 공격에 사용할 요청을 마우스 오른쪽 버튼으로 클릭하고 `Send to Intruder`를 선택합니다.
    *   `Intruder` > `Positions` 탭으로 이동합니다.
    *   `§` 기호로 표시된 공격 지점(Payload Positions)을 지정합니다. 보통 파라미터 값이 자동으로 선택됩니다.
    *   `Payloads` 탭에서 공격에 사용할 페이로드 목록(예: 숫자, 단어 리스트)을 설정합니다.
    *   `Start attack` 버튼을 눌러 공격을 시작하고, 응답 결과의 변화를 분석합니다.

### 사용 시 주의 사항
- Community Edition은 일부 기능이 제한됩니다 (예: 자동 스캔 기능, Intruder 속도). 모든 기능을 사용하려면 Professional Edition을 구매해야 합니다.
- Burp Suite 프록시 설정 후 해제하지 않은 경우 인터넷 연결에 문제가 발생할 수 있습니다. 사용 후에는 반드시 프록시 설정을 원래대로 되돌려야 합니다.
- 네트워크 가로채기 설정시 SSL 인증서 설정이 필요할 수 있습니다.

## 관련 URL
---
[PortSwigger 웹사이트](https://portswigger.net/burp/communitydownload)
[Web Security Academy (PortSwigger에서 제공하는 웹 보안 학습 플랫폼)](https://portswigger.net/web-security)
