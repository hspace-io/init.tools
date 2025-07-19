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
### Windows
`C:\Program Files\OWASP\Zed Attack Proxy` (기본 설치 경로)

### mac
`/Applications/OWASP ZAP.app`

### Linux
`~/ZAP_{version}` (압축 해제 경로)

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
1.  **프록시 설정**: ZAP을 실행하고 브라우저의 프록시 설정을 ZAP의 기본 프록시 주소(기본값: `127.0.0.1:8080`)로 변경합니다. HTTPS 트래픽을 분석하려면 ZAP의 CA 인증서를 브라우저에 설치해야 합니다.

2.  **수동 탐색 (Manual Explore)**: 브라우저를 통해 웹 애플리케이션을 탐색하면서 ZAP이 트래픽을 캡처하고 사이트 구조를 자동으로 빌드하도록 합니다. `Sites` 탭에서 탐색된 사이트 구조를 확인할 수 있습니다.

3.  **자동 스캔 (Automated Scan)**:
    *   `Quick Start` 탭에서 `Automated Scan`을 선택합니다.
    *   `URL to attack` 입력란에 스캔할 웹 애플리케이션의 URL을 입력하고 `Attack` 버튼을 클릭합니다.
    *   ZAP이 자동으로 크롤링 및 액티브 스캔을 수행하여 취약점을 탐지합니다.

4.  **액티브 스캔 (Active Scan)**: 특정 URL이나 파라미터에 대해 능동적인 공격을 수행하여 취약점을 탐지합니다.
    *   `Sites` 탭에서 스캔할 URL을 선택하고 마우스 오른쪽 버튼을 클릭한 후 `Attack > Active Scan`을 선택합니다.

5.  **경보 확인 (Alerts)**: `Alerts` 탭에서 탐지된 취약점 목록과 상세 정보를 확인할 수 있습니다. 위험도(High, Medium, Low, Informational)별로 분류됩니다.

6.  **보고서 생성**: `Report > Generate Report`를 선택하여 HTML, XML, PDF 등 다양한 형식으로 스캔 보고서를 생성할 수 있습니다.

### 실행 시 주의 사항
- Linux에서 CLI로 ZAP을 실행할 때 관리자 권한이 필요합니다.

## 관련 URL
---
[ZAP 공식 웹사이트](https://www.zaproxy.org/)
[ZAP 공식 웹사이트](https://www.zaproxy.org/)
