## 설명
---
`pwndbg`는 GDB(GNU Debugger)의 기능을 확장하여 리버스 엔지니어링 및 익스플로잇 개발에 특화된 기능을 제공하는 GDB 플러그인입니다. GDB의 기본 기능을 보완하고, 메모리 시각화, 취약점 분석 도구, 편리한 명령어 등을 통해 디버깅 경험을 크게 향상시킵니다.

## 설치 영역
---
`pwndbg`는 GDB의 플러그인이므로 별도의 설치 경로가 없습니다. 일반적으로 `~/.gdbinit` 파일에 pwndbg 스크립트를 소스(source)하도록 설정하여 GDB 실행 시 자동으로 로드됩니다.

## 주요 기능
---
- `향상된 디버깅 정보 표시`: 레지스터, 스택, 힙, 코드, 메모리 맵 등 핵심 디버깅 정보를 한눈에 볼 수 있도록 시각화하여 제공합니다.
- `취약점 분석 도구`: `checksec` (바이너리 보안 속성 확인), `rop` (ROP 가젯 검색), `heap` (힙 구조 분석) 등 익스플로잇 개발에 유용한 명령어를 제공합니다.
- `자동화된 정보 추출`: 함수 인자, 반환 주소, 스택 프레임 등 중요한 정보를 자동으로 파싱하여 표시합니다.
- `다양한 아키텍처 지원`: x86, x64, ARM, AArch64 등 다양한 CPU 아키텍처를 지원합니다.
- `확장성`: Python으로 작성되어 있어 사용자가 직접 플러그인을 개발하거나 기존 기능을 확장할 수 있습니다.

## 설치 방법
---
`pwndbg`는 GDB의 Python API를 사용하므로, GDB가 Python을 지원하도록 컴파일되어 있어야 합니다.

1.  **필수 패키지 설치**: 필요한 의존성 패키지를 설치합니다.
    ```sh
    sudo apt update
    sudo apt install python3 python3-pip python3-dev git libssl-dev libffi-dev build-essential
    ```

2.  **pwndbg 클론 및 설치**: GitHub에서 pwndbg 저장소를 클론하고 설치 스크립트를 실행합니다.
    ```sh
    git clone https://github.com/pwndbg/pwndbg
    cd pwndbg
    ./setup.sh
    ```
    *   `setup.sh` 스크립트는 필요한 Python 패키지를 설치하고 `~/.gdbinit` 파일에 pwndbg를 로드하는 설정을 추가합니다.

## 간단 가이드
---
1.  **GDB와 함께 pwndbg 실행**: pwndbg가 설치된 후, GDB를 실행하면 자동으로 pwndbg가 로드됩니다.
    ```sh
    gdb <실행 파일 경로>
    ```
    *   예시: `gdb ./a.out`

2.  **Context 정보 확인**: GDB가 실행되면 pwndbg는 자동으로 현재 레지스터, 스택, 코드, 메모리 등의 컨텍스트 정보를 보기 좋게 표시합니다.

3.  **Checksec**: 바이너리의 보안 속성을 확인합니다.
    ```sh
    checksec
    ```

4.  **Heap 정보**: 힙 관련 정보를 확인합니다. (힙 익스플로잇 시 유용)
    ```sh
    heap
    ```

5.  **Stack 정보**: 스택의 내용을 자세히 확인합니다.
    ```sh
    stack
    ```

6.  **ROP 가젯 검색**: 바이너리 내에서 ROP 가젯을 검색합니다.
    ```sh
    rop
    ```

7.  **GDB 기본 명령어 사용**: pwndbg는 GDB의 기능을 확장하는 것이므로, `b` (breakpoint), `r` (run), `n` (next), `s` (step), `c` (continue) 등 기존 GDB 명령어는 그대로 사용할 수 있습니다.

## 관련 URL
---
[pwndbg GitHub](https://github.com/pwndbg/pwndbg)
[pwndbg 문서](https://pwndbg.readthedocs.io/en/latest/)
