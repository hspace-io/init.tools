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
#### 프록시 설정
- Burp Suite는 기본적으로 로컬 프록시(`127.0.0.1:8080`)를 사용하기에 웹 브라우저의 프록시 설정을 Burp Suite 설정으로 변경해 줍니다.
	- `Firefox`: 설정 > 일반 > 네트워크 설정 > 설정... > 수동 프록시 구성 (HTTP 프록시: 127.0.0.1, 포트: 8080, "이 프록시 설정을 HTTPS에도 사용" 체크)
	- `Chrome`: 설정 > 시스템 > 컴퓨터 프록시 설정 열기 > 수동 프록시 설정 (프록시 서버 사용 켬, 주소: 127.0.0.1, 포트: 8080)

#### 인증서 설치
- HTTPS 트래픽을 가로채기 위해서는 Burp Suite의 CA 인증서를 브라우저에 설치해야 합니다.
	- Burp Suite에서 Proxy > Options > Proxy Listeners > Import / export CA certificate > Certificate in DER format > Next > 파일 저장
	- 브라우저의 인증서 관리자에서 "신뢰할 수 있는 루트 인증 기관"에 해당 인증서를 가져옵니다. (브라우저마다 방법이 다릅니다.)

### 사용 시 주의 사항
- Community Edition은 일부 기능이 제한됩니다 (예: 자동 스캔 기능). 모든 기능을 사용하려면 Professional Edition을 구매해야 합니다.
- Burp Suite 프록시 설정 후 해제하지 않은 경우 인터넷 연결에 문제가 발생할 수 있습니다.
- 네트워크 가로채기 설정시 SSL 인증서 설정이 필요할 수 있습니다.

## 관련 URL
---
[PortSwigger 웹사이트](https://portswigger.net/burp/communitydownload)
[Web Security Academy (PortSwigger에서 제공하는 웹 보안 학습 플랫폼)](https://portswigger.net/web-security)
