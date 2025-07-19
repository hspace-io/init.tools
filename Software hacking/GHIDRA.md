---
tags:
  - mac
  - linux
  - windows
  - reverse_engineering
  - pwnable
  - decompiler
  - multi_platform
---
## 설명
---
`Ghidra`는 미국 국가안보국(NSA)에서 개발한 오픈소스 소프트웨어 리버스 엔지니어링 프레임워크입니다.

## 설치 영역
---
### Windows
`{Download_path}/ghidra_{version}_PUBLIC/ghidraRun.bat`

### mac
- homebrew로 설치한 경우
`/opt/homebrew/Caskroom/ghidra/{version}/ghidra_{version}_PUBLIC/ghidraRun`

- github에서 다운 받은 경우
`/{Download_path}/ghidra_{version}_PUBLIC/ghidraRun`

## 주요 기능
---
- `디스어셈블 및 디컴파일`
- `코드 그래프 및 함수 흐름 시각화`
- `심볼/임포트/익스포트 분석`
- `스크립팅 및 확장`
- `자동화 및 배치 분석`
- `디버깅 지원`

## 설치 방법
---
### Windows
1. [Ghidra GitHub](https://github.com/NationalSecurityAgency/ghidra)에서 최신 버전 다운로드합니다.
2. 다운받은 파일의 압축을 해제하여 폴더 내부의 `ghidraRun.bat`을 실행시키면 됩니다.

### mac
- homebrew를 이용하는 경우
	1. 아래의 명령어를 터미널에 입력하여 설치합니다.
```sh
brew install --cask ghidra
```
	2. 터미널에 `ghidraRun`을 입력하여 Ghidra를 실행시킵니다.

- Ghidra GitHub에서 다운받는 경우
	1. [Ghidra GitHub](https://github.com/NationalSecurityAgency/ghidra)에서 최신 버전 다운로드합니다.
	2. 다운받은 파일의 압축을 해제하여 폴더 내부의 `ghidraRun`을 실행시키면 됩니다.

### 설치 시 주의 사항
- JAVA 21 이상(권장) 버전이 설치 되어있어야 합니다. 

## 간단 가이드
---
1.  **새 프로젝트 생성**: Ghidra를 실행하고 `File > New Project`를 선택합니다. `Non-Shared Project`를 선택하고 프로젝트 이름과 디렉토리를 지정합니다.

2.  **파일 임포트**: `File > Import File`을 선택하거나, 분석할 파일을 프로젝트 창으로 드래그 앤 드롭하여 가져옵니다. 임포트 설정 창이 나타나면 기본 설정을 유지하고 `OK`를 클릭합니다.

3.  **파일 분석**: 임포트가 완료되면 파일을 더블클릭하여 `CodeBrowser` 도구를 엽니다. 처음 열 때 파일을 분석할지 묻는 창이 나타나면 `Analyze`를 클릭합니다. 기본 분석 옵션을 그대로 사용하고 분석을 시작합니다.

4.  **코드 분석**: 분석이 완료되면 여러 창을 통해 프로그램을 분석할 수 있습니다.
    *   `Listing` (중앙): 디스어셈블된 코드를 보여줍니다.
    *   `Decompiler` (오른쪽): 선택된 함수의 C언어 의사 코드(Pseudo-code)를 보여줍니다. Ghidra의 가장 강력한 기능 중 하나입니다.
    *   `Symbol Tree` (왼쪽): 파일에 포함된 함수, 레이블, 클래스 등의 심볼 목록을 보여줍니다. 원하는 함수를 검색하고 더블클릭하여 해당 위치로 이동할 수 있습니다.
    *   `Function Graph` (상단 메뉴 `Window > Function Graph`): 함수의 흐름을 시각적인 그래프로 보여줍니다.

5.  **주석 및 이름 변경**: 분석 중 중요한 부분에 주석을 추가하거나(`;` 키), 함수 또는 변수 이름을 알아보기 쉽게 변경(`L` 키)할 수 있습니다.


## 관련 URL
---
[Ghidra GitHub](https://github.com/NationalSecurityAgency/ghidra)
[리버싱 입문자를 위한 Ghidra 튜토리얼](https://blog.hspace.io/posts/Ghidra-tutorial-for-reversing-beginners/)
