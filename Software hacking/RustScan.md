---
tags:
  - windows
  - mac
  - linux
  - scanning
  - network
  - cli_tool
  - multi_platform
  - port_scanner
---
## 설명
---
`RustScan`은 Rust로 작성된 초고속 포트 스캐너로, Nmap과 연동하여 빠른 포트 검색을 지원합니다.

## 설치 영역
---
`/usr/local/bin/rustscan`

## 주요 기능
---
- `초고속 포트 스캐닝`
- `스크립팅 엔진 지원`: Python, Lua, Shell 스크립트를 통한 자동화 및 확장 가능
- `Nmap 자동 연동`: 발견된 포트를 자동으로 Nmap으로 전달하여 상세 분석 수행
- `적응형 학습`: 사용자의 스캔 패턴을 학습하여 시간이 지날수록 성능 최적화
- `IPv6 및 CIDR 지원`: IPv4/IPv6 주소와 CIDR 표기법 지원
- `멀티 스레드 아키텍쳐`: 동시 다발적 스캔으로 속도 극대화

## 설치 방법
---
### mac
- 아래 명령어를 터미널에 입력하여 설치가 가능합니다.
```sh
brew install rustscan
```

## 간단 가이드
---
### 사용 시 주의 사항
- RustScan은 Nmap과 함께 사용해야 더 강력한 기능을 발휘합니다.

## 관련 URL
---
[RustScan 공식 웹사이트](https://rustscan.github.io/RustScan/)
