## 설명
---
`rp++`는 ROP(Return-Oriented Programming) 가젯을 바이너리 파일에서 빠르고 효율적으로 찾아주는 명령줄 도구입니다. 다양한 아키텍처와 파일 형식을 지원하며, 익스플로잇 개발 시 필요한 가젯을 신속하게 식별하는 데 사용됩니다.

## 설치 영역
---
`rp++`는 주로 단일 실행 파일 형태로 제공되므로, 특정 고정된 설치 경로가 없습니다. 사용자가 다운로드하여 압축을 해제한 디렉토리 또는 시스템 PATH에 추가된 위치에서 실행됩니다.

## 주요 기능
---
- `빠른 ROP 가젯 검색`: 바이너리 파일 내에서 `ret` 명령어로 끝나는 유용한 명령어 시퀀스(가젯)를 고속으로 검색합니다.
- `다양한 아키텍처 지원`: x86, x64, ARM, ARM64 등 여러 CPU 아키텍처의 바이너리를 분석할 수 있습니다.
- `다양한 파일 형식 지원`: PE(Windows), ELF(Linux), Mach-O(macOS) 등 주요 실행 파일 형식을 지원합니다.
- `세부 필터링`: 가젯의 길이, 포함할/제외할 명령어, 특정 섹션 등 다양한 조건으로 검색 결과를 필터링할 수 있습니다.
- `출력 형식 지정`: 검색 결과를 텍스트, JSON 등 다양한 형식으로 출력할 수 있습니다.

## 설치 방법
---
`rp++`는 미리 컴파일된 바이너리 형태로 제공되므로, 다운로드 후 바로 사용할 수 있습니다.

1.  **rp++ 다운로드**: [rp++ GitHub Releases](https://github.com/0vercl0k/rp/releases) 페이지에서 운영체제에 맞는 최신 버전을 다운로드합니다.
    *   예시: `rp-lin-x64` (Linux 64비트), `rp-win-x64.exe` (Windows 64비트), `rp-osx-x64` (macOS 64비트)

2.  **압축 해제 및 실행**: 다운로드한 파일을 압축 해제한 후, 실행 권한을 부여하고 사용합니다.
    ```sh
    # Linux/macOS
    chmod +x rp-lin-x64 # 또는 rp-osx-x64
    ./rp-lin-x64 --help

    # Windows
    rp-win-x64.exe --help
    ```

3.  **PATH 환경 변수 추가 (선택 사항)**: `rp++` 실행 파일을 시스템 PATH에 추가하면 어느 디렉토리에서든 `rp++` 명령어를 사용할 수 있습니다.

## 간단 가이드
---
1.  **기본 가젯 검색**: 바이너리 파일에서 모든 ROP 가젯을 검색합니다.
    ```sh
    ./rp++ --file <바이너리 파일 경로>
    ```
    *   예시: `./rp-lin-x64 --file ./a.out`

2.  **특정 명령어 포함 가젯 검색**: 특정 명령어를 포함하는 가젯만 검색합니다.
    ```sh
    ./rp++ --file <바이너리 파일 경로> --search "pop rdi; ret"
    ```
    *   예시: `./rp-lin-x64 --file ./a.out --search "pop rdi; ret"`

3.  **가젯 길이 제한**: 가젯의 최대 길이를 제한하여 검색합니다.
    ```sh
    ./rp++ --file <바이너리 파일 경로> --max-instruction 5
    ```
    *   예시: `./rp-lin-x64 --file ./a.out --max-instruction 5` (최대 5개의 명령어로 구성된 가젯 검색)

4.  **출력 형식 지정**: 검색 결과를 JSON 형식으로 출력할 수 있습니다.
    ```sh
    ./rp++ --file <바이너리 파일 경로> --json
    ```

5.  **섹션 지정**: 특정 섹션 내에서만 가젯을 검색합니다.
    ```sh
    ./rp++ --file <바이너리 파일 경로> --section .text
    ```

## 관련 URL
---
[rp++ GitHub](https://github.com/0vercl0k/rp)
[ROP (Return-Oriented Programming) 설명](https://en.wikipedia.org/wiki/Return-oriented_programming)

