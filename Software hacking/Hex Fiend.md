---
tags:
  - mac
  - hex_editor
  - debugging
---
## 설명
---
`Hex Fiend`는 macOS 전용 오픈소스 hex editor입니다.

## 설치 영역
---
`/Applications/Hex Fiend.app`

## 주요 기능
---
- `삽입, 삭제, 재배치`: 파일의 임의 위치에서 바이트 단위로 자유롭게 데이터 삽입/삭제/이동 가능
- `이진 비교 (binary Diff)`
- `데이터 인스펙터`
- `바이너리 템플릿`: 파일 구조를 스크립트로 시각화

## 설치 방법
---
- [Hex Fiend 웹사이트](https://hexfiend.com/)에서 다운 받는 방법
	1. [Hex Fiend 웹사이트](https://hexfiend.com/)에서 설치 파일을 다운 받습니다.
	2. .dmg 파일을 실행하여 설치를 진행합니다.

- App Store를 이용하는 방법
	1. App Store에서 Hex Fiend를 검색하고 설치를 누르면 됩니다,.

- homebrew를 이용하는 방법
	1. 터미널에 다음 명령어를 입력합니다.
```sh
brew install --cask hex-fiend
```

- GitHub를 이용하는 방법
	1. [Hex Fiend github](https://github.com/HexFiend/HexFiend)의 Releases 페이지에서 원하는 버전을 다운 받습니다.
	2. .dmg 파일을 실행하여 설치를 진행합니다.

### 설치 시 주의 사항
- GitHub에서 pre-release버전을 다운 받은 경우 프로그램이 불안정 할 수 있습니다.

## 간단 가이드
---
1.  **파일 열기**: `File > Open` 메뉴를 통해 분석할 파일을 열거나, 파일을 Hex Fiend 아이콘으로 드래그 앤 드롭합니다.
2.  **데이터 탐색**: 스크롤하여 파일의 내용을 탐색합니다. 왼쪽에는 오프셋(주소), 가운데에는 16진수 데이터, 오른쪽에는 ASCII 표현이 표시됩니다.
3.  **데이터 편집**: 원하는 위치의 16진수 값이나 ASCII 문자를 직접 클릭하여 수정할 수 있습니다. 변경된 내용은 빨간색으로 표시됩니다.
4.  **데이터 검색**: `Edit > Find > Find` (Cmd+F)를 사용하여 16진수 시퀀스나 텍스트 문자열을 검색할 수 있습니다.
5.  **데이터 인스펙터 사용**: `View > Data Inspector` (Cmd+Opt+I)를 활성화하면, 현재 커서 위치의 데이터를 다양한 형식(정수, 부동소수점, 문자 인코딩 등)으로 해석하여 보여줍니다.
6.  **이진 비교**: `File > Compare` 메뉴를 통해 두 개의 파일을 열고 차이점을 시각적으로 비교할 수 있습니다. 다른 부분은 색상으로 강조 표시됩니다.


## 관련 URL
---
[Hex Fiend 웹사이트](https://hexfiend.com/)
[Hex Fiend github](https://github.com/HexFiend/HexFiend)
[Hex Fiend App Store](https://apps.apple.com/kr/app/hex-fiend/id1342896380?mt=12)

