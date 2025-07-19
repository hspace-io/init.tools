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


## 관련 URL
---
[Ghidra GitHub](https://github.com/NationalSecurityAgency/ghidra)
[리버싱 입문자를 위한 Ghidra 튜토리얼](https://blog.hspace.io/posts/Ghidra-tutorial-for-reversing-beginners/)
