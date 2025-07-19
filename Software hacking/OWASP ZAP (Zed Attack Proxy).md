---
tags:
  - windows
  - mac
  - linux
  - web_security
  - debugging
  - webapp
  - multi_platform
---
## 설명
---
`OWSAP ZAP`은 웹 애플리케이션의 보안 취약점을 자동/수동으로 진단하는 오픈소스 DAST(Dynamic Application Security Testing)도구입니다.

## 설치 영역
---


## 주요 기능
---
- `자동 스캐닝`: 웹사이트를 크롤링하고, SQL Injection, XSS 등 다양한 취약점 자동 진단
- `프록시 기능`: 브라우저와 웹 서버 사이에서 트래픽을 중계하고, 요청/응답 실시간 분석 수정 가능
- `Active/Passive Scan`
	- Active Scan: 실제 공격 페이로드를 주입해 취약점 존재 여부 확인
	- Passive Scan: 트래픽을 분석해 위험 신호 탐지
- `경보 및 리포트`: 탐지된 취약점에 대해 위험도별로 경보 생성, 상세 리포트 제공
- `실시간 트래픽 분석 및 수정`: 요청/응답 헤더, 바디 수저, 재전송, 리플레이 등 지원
- `API/자동화 지원`: REST API 제공, CI/CD 파이프 라인 연동 가능
- `스캔 정책/설정 커스터마이즈`: 스캔 정책 템플릿 저장 및 재사용, 스캔 강도/번위 조절

## 설치 방법
---
### Windows
1. [ZAP 공식 웹사이트](https://www.zaproxy.org/)에서 환경에 맞는 설치 파일을 다운 받고 `ZAP_{version}_windows.exe`를 실행시킵니다.
2. 설치 마법사를 따라 설치를 진행합니다.

### Linux
- [ZAP GitHun](https://github.com/zaproxy/zaproxy)에서 ZAP을 다운 받고 압축해제하여 사용하시면 됩니다.
```sh
wget https://github.com/zaproxy/zaproxy/releases/download/v{version}/ZAP_{version}_Linux.tar.gz

tar -zxvf ZAP_{version}_Linux.tar.gz
```

### mac
- 아래의 명령어를 터미널에 입력하여 설치합니다.
```sh
brew install --cask zap
```

### 설치 시 주의 사항
- ZAP 설치를 위해서는 JAVA를 사전에 설치해야합니다.

## 간단 가이드
---
### 실행 시 주의 사항
- Linux에서 CLI로 ZAP을 실행할 때 관리자 권한이 필요합니다.

## 관련 URL
---
[ZAP 공식 웹사이트](https://www.zaproxy.org/)
[ZAP 공식 웹사이트](https://www.zaproxy.org/)
