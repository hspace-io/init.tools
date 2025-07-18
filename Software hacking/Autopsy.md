---
tags:
  - mac
  - windows
  - linux
  - forensic
---
## 설명
---
`Autopsy`는 디지털 포렌식 분석을 위한 GUI 기반 오픈소스 도구로, 사용자가 디스크 이미지를 분석하고 파일 복구, 타임라인 생성, 이메일 분석 등을 수행할 수 있도록 지원합니다. 이는 법적 디지털 증거 수집 및 조사 목적으로 널리 사용됩니다.

## 설치 영역
---
### Linux
`/`

### mac
`/`

### Windows
`/`

## 주요 기능
---
- 디스크 이미지 분석
- 삭제된 파일 복구
- 웹 브라우저 기록 및 이메일 분석
- 타임라인 생성 및 활동 추적

## 설치 방법
---
### 1. Autopsy 설치
- [Autopsy 공식 다운로드 페이지](https://www.autopsy.com/download/)에서 설치 파일을 다운로드 합니다.
- macOS에서 Autopsy를 실행하려면 `The Sleuth Kit`을 설치해야 합니다.
```sh
brew install sleuthkit
```
### 2. Autopsy 실행
```sh
sh autopsy
```

### 3. 설치 확인
- Autopsy를 실행하여 새 케이스를 생성하고 디스크 이미지를 불러와 분석 작업이 정상적으로 수행되는지 확인하세요.

### 주의 사항
- Autopsy는 Java 환경이 필요합니다. Java 8 이상이 설치되어 있어야 합니다.
- 파일 시스템 포멧 및 디스크 이미지 지원 여부는 `The Sleuth Kit`에 의존합니다.


## 간단 가이드
---
1.  **새 케이스 생성**: Autopsy를 실행하고 `Create New Case`를 선택합니다. 케이스 이름과 저장될 디렉토리를 지정합니다.
2.  **데이터 소스 추가**: 케이스가 생성되면 데이터 소스를 추가하라는 메시지가 표시됩니다. `Add Data Source`를 클릭하고 분석할 디스크 이미지 파일(예: `.dd`, `.e01`) 또는 로컬 디스크를 선택합니다.
3.  **인제스트 모듈 설정**: 데이터 소스를 추가한 후, 분석을 위해 실행할 `Ingest Modules`를 선택합니다. 예를 들어, `Recent Activity`(최근 활동), `Keyword Search`(키워드 검색), `File Type Identification`(파일 유형 식별) 등을 선택할 수 있습니다.
4.  **분석 진행**: 인제스트 모듈이 실행되면서 파일 시스템을 분석하고, 삭제된 파일을 복구하며, 아티팩트를 추출합니다. 이 과정은 데이터 소스의 크기에 따라 시간이 걸릴 수 있습니다.
5.  **결과 확인**: 분석이 완료되면 왼쪽 트리 메뉴에서 다양한 항목을 탐색할 수 있습니다.
    *   `File Views`: 파일 유형, 삭제된 파일, 문서 등을 기준으로 파일을 봅니다.
    *   `Data Artifacts`: 웹 기록, 레지스트리, 이메일 등 추출된 아티팩트를 확인합니다.
    *   `Timeline`: 파일 시스템 활동을 시간순으로 시각화하여 분석합니다.


## 관련 URL
---
[Autopsy 공식 웹 사이트](https://www.autopsy.com/)
