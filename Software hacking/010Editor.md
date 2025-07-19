---
tags:
  - mac
  - windows
  - forensic
  - debugging
  - reverse_engineering
---
## 설명
---
`010 Editor`는 SweetScape Software에서 개발한 전문가용 상용 헥스 에디터 및 텍스트 에디터입니다. 2003년 Graeme Sweet에 의해 처음 개발되었으며, 원래 대용량 해양 시각화 데이터셋의 문제를 해결하기 위해 설계되었습니다. 가장 큰 특징은 Binary Template 기능으로, 280개 이상의 다양한 바이너리 포맷을 구조화해서 볼 수 있어 디지털 포렌식, 리버스 엔지니어링 등에 널리 사용됩니다.

## 설치 영역
---
### Windows
`C:\Program Files\010 Editor` 기본 설치 경로, 사용자가 변경 가능

### mac


## 주요 기능
---
- `Binary Tempalte`: 160개 이상의 파일 포맷(zip, mp3, wav, pdf, exe, elf, jpg, pcap 등)을 구조화 해서 분석 가능
- `하드 드라이브 직접 편집`: 50GB 이상의 텍스트 파일, 8EB(엑사바이트)의 파일 처리 가능
- `스크립팅`: C/C++와 유사한 언어로 스크립팅 지원
- `체크섬/해시 계산`: CRC-16, CRC-32, Adler32, MD2, MD4, MD5, RIPEMD160, SHA-1, SHA-256, SHA-512, TIGER 지원
- `다양한 문자 인코딩`:  ASCII, Unicode, UTF-8 등 30가지 문자 인코딩 지원 및 변환
- `컬럼 모드 편집`: 텍스트의 특정 열만 선택하여 편집 가능
- `무제한 실행 undo/redo`
- `온라인 저장소`: Binary Template과 스크립트를 온라인으로 공유하고 다운로드 가능

## 설치 방법
---
### Windows
- [010 Editor 공식 웹사이트](https://www.sweetscape.com/download/010editor/)에서 환경에 맞는 설치 파일을 다운 받습니다.
- `010EditorWin64Installer{version}.exe`을 실행하여 설치를 진행합니다.
### mac
- 아래 명령어를 터미널에 입력하여 설치할 수 있습니다.
```sh
brew install --cask 010-editor
```

### 설치 시 주의 사항
- 010 Editor는 유료 프로그램이지만, 무료 체험판을 이용할 수 있습니다. 
## 간단 가이드
---
1.  **파일 열기**: `File > Open` 메뉴를 통해 분석할 파일을 엽니다.
2.  **바이너리 템플릿 적용**:
    *   `Templates > Template Repository`로 이동하여 원하는 파일 형식의 템플릿을 찾습니다. (예: `ZIP.bt`, `PNG.bt`)
    *   템플릿을 선택하고 `Install` 버튼을 눌러 설치합니다.
    *   설치된 템플릿은 `Templates` 메뉴에 추가됩니다. 해당 템플릿을 실행하면 파일 구조가 파싱되어 보입니다.
3.  **데이터 분석**: 템플릿을 적용하면 헥스 뷰 하단에 `Template Results` 창이 나타납니다. 이 창에서 파일의 구조(헤더, 청크 등)를 트리 형태로 확인하고 각 필드의 값을 쉽게 분석할 수 있습니다.
4.  **스크립트 실행**: `Scripts` 메뉴에서 내장된 스크립트(예: 해시 계산, 인코딩 변환)를 실행하거나, 직접 작성한 스크립트를 실행하여 분석을 자동화할 수 있습니다.


## 관련 URL
---
[010 Editor 공식 웹사이트](https://www.sweetscape.com/download/010editor/)