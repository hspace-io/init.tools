---
tags:
  - windows
  - mac
  - linux
  - network
  - scanning
  - port_scanner
  - multi_platform
  - cli_tool
---
## 설명
---
`Nmap`은 네트워크 탐색과 보안 진단을 위한 오픈소스 네트워크 스캐너입니다.네트워크 상의 호스트, 서비스, 운영체제, 포트, 취약점 등을 십겨하고, 보안 점검 및 자산 관리, 네트워크 인벤토리 구축 등 다양한 목적으로 활용됩니다.

## 설치 영역
---

## 주요 기능
---
- `호스트 탐지`: 네트워크 내 활성화 된 시스템 탐색 (ICMP, TCP 등)
- `포트 스캔`
- `서비스 및 버전 식별`: 각 포트에서 동작하는 서비스의 종류와 버전 확인
- `운영체제 및 디바이스 유형 탐지`: 패킷 응답 패턴을 분석해 OS, 장비 유형, MAC 주소 등 식별
- `Nmap Scripting Engine(NSE)`: Lua 기반 스크립트로 취약점 진단, 추가 서비스 탐지 등 자동화
- `GUI`: Zenmap(공식 GUI 앱) 사용시 가능

## 설치 방법
---
### Windows
1. [nmap 웹사이트](https://nmap.org/)에 접속해서 Nmap 환경에 맞는 설치 파일 다운로드
2. 설치 마법사에 따라 설치를 진행
	- `nmap-{version}-setup.exe` 실행
3. nmap 명령어를 이용해서 사용 가능
	- powershell에서 명령어 사용 가능합니다.

### Linux
- 아래 명령어를 터미널에 입력하여 설치합니다.
```sh
sudo apt install nmap
```

### mac
- 아래 명령어를 터미널에 입력하여 설치합니다.
```sh
brew install nmap
```


## 간단 가이드
---


## 관련 URL
---
[nmap 웹사이트](https://nmap.org/)
