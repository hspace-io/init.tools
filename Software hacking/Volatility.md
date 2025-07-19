---
tags:
  - windows
  - mac
  - linux
  - forensic
  - memory_analysis
  - multi_platform
---
## 설명
---
`Volatility`는 메모리 덤프 분석을 위한 업계 표준 디지털 포렌식 도구 프레임워크 입니다. 메모리 내의 실행 프로세스, 네트워크 연결, DLL, 레지스트리 키 등 중요한 데이터를 복구 및 분석하는데 사용됩니다.

## 설치 영역
---
`/path/to/site-package/vollatility`

## 주요 기능
---
- 메모리 덤프 분석
- 악성코드 탐지 및 제거
- 디지털 포렌식 사고 대응

## 설치 방법
---
### Python
- 아래의 명령어들을 터미널에 입력하여 설치 할 수 있습니다.
```sh
git clone https://github.com/volatilityfoundation/volatility3.git
cd vollatility3
python3 setup.py install
```

## 간단 가이드
---
1.  **메모리 덤프 준비**: 분석할 메모리 덤프 파일(예: `.raw`, `.mem`, `.vmem`)을 준비합니다.

2.  **프로파일 확인**: 메모리 덤프의 운영체제 및 버전에 맞는 프로파일을 확인해야 합니다. `imageinfo` 플러그인을 사용하여 적절한 프로파일을 추천받을 수 있습니다.
    ```sh
    python3 vol.py -f <메모리 덤프 파일 경로> windows.info.Info
    ```
    *   예시: `python3 vol.py -f memory.raw windows.info.Info`
    *   출력된 `Suggested Profile(s)` 중에서 가장 적절한 것을 선택합니다.

3.  **주요 플러그인 사용 예시**:
    *   **실행 중인 프로세스 목록 확인**: `pslist` 플러그인을 사용하여 메모리 덤프 시점에 실행 중이던 모든 프로세스를 나열합니다.
        ```sh
        python3 vol.py -f <메모리 덤프 파일 경로> --profile=<프로파일 이름> windows.pslist
        ```
        *   예시: `python3 vol.py -f memory.raw --profile=Win7SP1x64 windows.pslist`

    *   **네트워크 연결 정보 확인**: `netscan` 플러그인을 사용하여 활성 네트워크 연결 및 열린 포트를 확인합니다.
        ```sh
        python3 vol.py -f <메모리 덤프 파일 경로> --profile=<프로파일 이름> windows.netscan
        ```

    *   **DLL 목록 확인**: `dlllist` 플러그인을 사용하여 특정 프로세스에 로드된 DLL 목록을 확인합니다.
        ```sh
        python3 vol.py -f <메모리 덤프 파일 경로> --profile=<프로파일 이름> windows.dlllist -p <PID>
        ```

    *   **레지스트리 하이브 목록 확인**: `hivelist` 플러그인을 사용하여 로드된 레지스트리 하이브 목록을 확인합니다.
        ```sh
        python3 vol.py -f <메모리 덤프 파일 경로> --profile=<프로파일 이름> windows.hivelist
        ```

    *   **명령어 히스토리 확인**: `cmdline` 또는 `consoles` 플러그인을 사용하여 명령 프롬프트 또는 PowerShell에서 실행된 명령어 히스토리를 확인합니다.
        ```sh
        python3 vol.py -f <메모리 덤프 파일 경로> --profile=<프로파일 이름> windows.cmdline
        ```

- Volatility를 실행한 후 사용 가능한 플러그인 목록을 확인하려면 아래의 명령어를 실행하시면 됩니다.
```sh
python3 vol.py -h
```

## 관련 URL
---
[Volatility 공식 GitHub 저장소](https://github.com/volatilityfoundation/volatility3)
