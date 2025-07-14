---
tags:
  - mac
  - windows
  - linux
  - forensic
  - metadata
  - cli_tool
---
## 설명
---
`ExifTool`은 메타데이터를 읽고, 작성하고 수정할 수 있는 도구입니다. 이미지, 비디오, 오디오, 문서 파일 등의 메타데이터를 분석하는 데 사용합니다.

## 설치 영역
---
### Windows
`해당 프로그램은 윈도우에서는 portable파일을 지원함으로, 설치하지 않고 사용이 가능합니다.`

### Linux
``/usr/local/bin/exiftool``

### mac
`/opt/homebrew/bin/exiftool`

## 주요 기능
---
- `디지털 포렌식에서 이미지 및 문서 파일의 메타데이터 분석`
- 사진 및 미디어 파일의 메타데이터 편집 및 삭제
- 자동화된 파일 정리 및 스크립트 구현

## 설치 방법
---
### Windows
1. [ExifTool 웹사이트에 접속](https://exiftool.org/index.html)하여 환경에 맞는 파일을 다운로드 합니다.
2. 다운 받은 파일의 압축을 해제 합니다.

### Linux
1. 터미널에 아래 명령어를 입력하시면 됩니다.
```sh
sudo apt install libimage-exiftool-perl
```

### mac
1. `homebrew`를 이용하는 경우 아래의 명령어를 터미널에 입력하시면 됩니다.
```sh
brew install exiftool
```


## 간단 가이드
---
### 사용 시 주의 사항
- 일부 파일 형식에서는 메타데이터 수정이 제한 될 수 있습니다.
- 원본 파일을 보호하기 위해 백업 옵션(-overwrite_original)을 주의해서 사용할 것을 권장드립니다.

## 관련 URL
---
[ExifTool 웹사이트에 접속](https://exiftool.org/index.html)
