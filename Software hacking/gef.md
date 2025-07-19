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
GEF는 GDB의 플러그인이므로 별도의 설치 경로가 없습니다. 일반적으로 `~/.gdbinit` 파일에 GEF 스크립트를 소스(source)하도록 설정하여 GDB 실행 시 자동으로 로드됩니다.

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
1.  **GDB와 함께 GEF 실행**: GEF가 설치된 후, GDB를 실행하면 자동으로 GEF가 로드됩니다.
    ```sh
    gdb <실행 파일 경로>
    ```
    *   예시: `gdb ./a.out`

2.  **Context 정보 확인**: GDB가 실행되면 GEF는 자동으로 현재 레지스터, 스택, 코드, 메모리 등의 컨텍스트 정보를 보기 좋게 표시합니다.

3.  **Checksec**: 바이너리의 보안 속성을 확인합니다.
    ```sh
    checksec
    ```

4.  **Heap 정보**: 힙 관련 정보를 확인합니다. (힙 익스플로잇 시 유용)
    ```sh
    heap
    ```

5.  **Telescope**: 스택 또는 메모리 주소의 내용을 자세히 확인합니다.
    ```sh
    telescope $rsp # 스택 포인터가 가리키는 곳의 내용 확인
    telescope 0x12345678 # 특정 주소의 내용 확인
    ```

6.  **ROP 가젯 검색**: 바이너리 내에서 ROP 가젯을 검색합니다.
    ```sh
    ropper
    ```

7.  **GDB 기본 명령어 사용**: GEF는 GDB의 기능을 확장하는 것이므로, `b` (breakpoint), `r` (run), `n` (next), `s` (step), `c` (continue) 등 기존 GDB 명령어는 그대로 사용할 수 있습니다.

## 관련 URL
---
[GEF Github](https://github.com/hugsy/gef)
[GEF Document](https://hugsy.github.io/gef/install/)
