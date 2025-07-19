---
tags:
  - linux
  - mac
  - windows
  - pwnable
  - reverse_engineering
  - gadget_finder
  - exploit_analysis
---
## 설명
---
`ROPgadget`은 Return-Oriented Programming (ROP) 공격에 사용될 수 있는 가젯(gadget)을 바이너리 파일에서 찾아주는 도구입니다. ROP 공격은 스택 버퍼 오버플로우와 같은 취약점을 이용하여 프로그램의 제어 흐름을 조작할 때 사용되며, 실행 가능한 코드 영역에 직접 코드를 삽입하는 대신, 이미 존재하는 코드 조각(가젯)들을 연결하여 원하는 동작을 수행하게 합니다.

## 설치 영역
---
`ROPgadget`은 Python 패키지로 설치되므로, 특정 고정된 설치 경로가 없습니다. Python의 `site-packages` 디렉토리에 설치됩니다.

## 주요 기능
---
- `ROP 가젯 검색`: 바이너리 파일 내에서 `ret` 명령어로 끝나는 유용한 명령어 시퀀스(가젯)를 검색합니다.
- `다양한 아키텍처 지원`: x86, x64, ARM, ARM64 등 다양한 CPU 아키텍처의 바이너리를 분석할 수 있습니다.
- `세부 필터링`: 가젯의 길이, 포함할/제외할 명령어 등 다양한 조건으로 검색 결과를 필터링할 수 있습니다.
- `바이너리 정보 추출`: 바이너리의 섹션 정보, 심볼 정보 등을 함께 제공합니다.

## 설치 방법
---
`ROPgadget`은 Python 기반 도구이므로 `pip`를 사용하여 설치합니다.

1.  **Python 및 pip 설치**: 시스템에 Python과 pip가 설치되어 있어야 합니다.
2.  **ROPgadget 설치**: 터미널에서 다음 명령어를 실행합니다.
    ```sh
    pip install ropgadget
    ```

## 간단 가이드
---
1.  **기본 가젯 검색**: 바이너리 파일에서 모든 ROP 가젯을 검색합니다.
    ```sh
    ROPgadget --binary <바이너리 파일 경로>
    ```
    *   예시: `ROPgadget --binary ./a.out`

2.  **특정 명령어 포함 가젯 검색**: 특정 명령어를 포함하는 가젯만 검색합니다.
    ```sh
    ROPgadget --binary <바이너리 파일 경로> --only "pop|ret"
    ```
    *   예시: `ROPgadget --binary ./a.out --only "pop|ret"` (pop과 ret 명령어를 포함하는 가젯 검색)

3.  **가젯 길이 제한**: 가젯의 최대 길이를 제한하여 검색합니다.
    ```sh
    ROPgadget --binary <바이너리 파일 경로> --max-inst 5
    ```
    *   예시: `ROPgadget --binary ./a.out --max-inst 5` (최대 5개의 명령어로 구성된 가젯 검색)

4.  **바이너리 정보 확인**: 바이너리의 헤더, 섹션, 심볼 정보 등을 확인합니다.
    ```sh
    ROPgadget --info <바이너리 파일 경로>
    ```

5.  **출력 형식 지정**: 검색 결과를 JSON 형식으로 출력할 수 있습니다.
    ```sh
    ROPgadget --binary <바이너리 파일 경로> --json
    ```

## 관련 URL
---
[ROPgadget GitHub](https://github.com/JonathanSalwan/ROPgadget)
[Return-Oriented Programming (Wikipedia)](https://en.wikipedia.org/wiki/Return-oriented_programming)
