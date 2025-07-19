---
tags:
  - linux
  - debugging
  - pwnable
  - cli_tool
  - multi_platform
---
## 설명
---
GEF(GDB Enhanced Features)는 GDB를 위한 확장 플러그인입니다. Python API를 활용해 GDB의 디버깅 경험을 대폭 개선하면, 다양한 아키텍처에서 동작합니다.

## 설치 영역
---


## 주요 기능
---
- `디버깅 정보 시각화`
- `익스플로잇/리버스 엔지니어링 특화 명령어`
	- `context` : 현재 실행 상태(레지스터, 스택, 코드, 메모리 등) 한 화면에 요약
	- `checksec` : 바이너리의 보안 속성(RELRO, PIE, NX, canary 등) 분석
	- `heap`, `telescope`, `elf-info`, `got`, `ropper` 등 고급 분석 명령어
	- 포맷 스트링 취약점, 힙 구조, GOT/PLT, UEFI, OPTEE 등 다양한 환경 지원
- `확장`
	- 커스텀 플러그인 및 명령어 추가, 커뮤니티 플러그인 사용 가능
- `실행 중 시스템 콜 인자 자동 표시, 메모리/레지스터/플래그 등 상세 정보 제공`
- `ASLR, 페이지 권한, ELF 헤더 등 시스템/프로세스 상태 분석`

## 설치 방법
---
### Linux
아래의 명령어를 터미널에 입력하여 설치 가능합니다.
- 빠른 설치
```sh
bash -c "$(curl -fsSL https://gef.blah.cat/sh)"
# 또는
bash -c "$(wget https://gef.blah.cat/sh -O -)"
```

- 수동 설치
```sh
git clone https://github.com/hugsy/gef.git
echo "source /path/to/gef.py" >> ~/.gdbinit
```


## 간단 가이드
---


## 관련 URL
---
[GEF Github](https://github.com/hugsy/gef)
[GEF Document](https://hugsy.github.io/gef/install/)
