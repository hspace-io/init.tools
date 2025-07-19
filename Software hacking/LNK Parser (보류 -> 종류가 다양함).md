---
tags:
  - windows
  - forensic
  - artifact_analysis
  - metadata
---
## 설명
---
`LNK Parser`는 Windows 단축 파일(.lnk, Microsoft Shell Link)의 내부 구조와 메타데이터를 분석하는 도구 또는 라이브러리 입니다.

## 설명
---
`LNK Parser`는 Windows 단축 파일(.lnk, Microsoft Shell Link)의 내부 구조와 메타데이터를 분석하는 도구 또는 라이브러리입니다. LNK 파일은 사용자가 파일, 폴더, 애플리케이션 등에 접근할 때 자동으로 생성되며, 원본 파일의 경로, 생성/수정 시간, 접근 시간, 볼륨 정보, 네트워크 경로 등 다양한 정보를 포함하고 있어 디지털 포렌식 조사에서 중요한 아티팩트로 활용됩니다.

## 설치 영역
---
`LNK Parser는 특정 단일 도구를 지칭하기보다는 LNK 파일을 분석하는 다양한 도구 및 라이브러리를 포괄합니다. 따라서 설치 경로는 사용되는 도구에 따라 다릅니다.`

## 주요 기능
---
- `원본 파일 경로 추출`: 단축 파일이 가리키는 원본 파일의 로컬 또는 네트워크 경로를 파싱합니다.
- `타임스탬프 분석`: LNK 파일 자체의 생성/수정/접근 시간뿐만 아니라, 원본 파일의 타임스탬프 정보도 추출합니다.
- `볼륨 정보`: 원본 파일이 위치했던 드라이브의 볼륨 시리얼 번호, 이름 등을 확인합니다.
- `네트워크 정보`: 원본 파일이 네트워크 공유 폴더에 있었을 경우, 해당 네트워크 경로 및 MAC 주소 등의 정보를 추출합니다.
- `대상 파일의 크기 및 속성`: 원본 파일의 크기, 속성(읽기 전용, 숨김 등) 정보를 파싱합니다.
- `Hotlink 정보`: 원본 파일이 삭제되거나 이동된 경우에도 마지막으로 접근했던 경로를 추적할 수 있는 정보를 제공합니다.

## 설치 방법
---
LNK 파일을 분석하는 도구는 다양하며, 주로 다음과 같은 형태로 제공됩니다.

### 1. 독립 실행형 도구 (Standalone Tools)
*   **LnkParse3**: Python으로 작성된 LNK 파일 파서로, CLI 환경에서 사용됩니다. GitHub에서 소스 코드를 다운로드하여 실행하거나, `pip`로 설치할 수 있습니다.
    ```bash
    pip install lnkparse3
    ```
*   **Lnk Parser (Eric Zimmerman's Tools)**: Windows 환경에서 GUI 또는 CLI로 사용할 수 있는 강력한 포렌식 도구 모음 중 하나입니다. 공식 웹사이트에서 다운로드하여 사용합니다.

### 2. 포렌식 프레임워크 내장 기능
*   **Autopsy, EnCase, FTK Imager**: 이러한 통합 포렌식 도구들은 LNK 파일 분석 기능을 내장하고 있어, 디스크 이미지 분석 시 자동으로 LNK 파일을 파싱하고 관련 정보를 보여줍니다.

### 3. Python 라이브러리
*   **python-lnk**: LNK 파일을 파싱하기 위한 Python 라이브러리입니다. 스크립트 작성 시 유용합니다.
    ```bash
    pip install python-lnk
    ```

## 간단 가이드
---
여기서는 `LnkParse3` (Python CLI 도구)를 예시로 간단한 사용법을 설명합니다.

1.  **LNK 파일 준비**: 분석할 `.lnk` 파일을 준비합니다.

2.  **LnkParse3 실행**: 터미널 또는 명령 프롬프트에서 다음 명령어를 실행합니다.
    ```bash
    lnkparse3 <LNK 파일 경로>
    ```
    *   예시: `lnkparse3 C:\Users\user\Desktop\document.lnk`

3.  **결과 확인**: 실행하면 LNK 파일에 포함된 다양한 메타데이터가 JSON 형식으로 출력됩니다. 주요 정보는 다음과 같습니다.
    *   `target_path`: 원본 파일의 경로
    *   `creation_time`, `access_time`, `write_time`: LNK 파일 및 원본 파일의 타임스탬프
    *   `volume_information`: 볼륨 시리얼 번호, 이름 등
    *   `network_share_info`: 네트워크 공유 정보 (있는 경우)

#### 다른 도구 사용 시
*   **GUI 기반 도구 (예: Eric Zimmerman's Lnk Parser)**: 도구를 실행한 후, LNK 파일을 로드하거나 드래그 앤 드롭하여 GUI에서 시각적으로 정보를 확인합니다.
*   **통합 포렌식 도구**: 디스크 이미지를 로드하면, 해당 도구가 자동으로 LNK 파일을 분석하여 관련 아티팩트 섹션에 정보를 표시합니다.

## 관련 URL
---
[LnkParse3 GitHub](https://github.com/fireeye/flare-fakenews/tree/master/LnkParse3)
[Eric Zimmerman's Tools (Lnk Parser 포함)](https://ericzimmerman.github.io/#!index.md)
[Microsoft Shell Link (.LNK) Binary File Format](https://learn.microsoft.com/en-us/openspecs/windows_protocols/ms-shllink/16cb4ca1-9337-49c4-8910-ce4149c6105d)
