---
tags:
  - windows
  - mac
  - linux
  - reverse_engineering
  - android
  - apk_analysis
  - multi_platform
---
## 설명
---
`JADX`는 Android 애플리케이션의 DEX(Dalvik Executable) 및 APK 파일을 Java 소스 코드로 디컴파일 하는 오픈 소스 도구입니다.

## 설치 영역
---


## 주요 기능
---
- `DEX, APK, AAB, JAR 등 다양한 파일을 Java 소스 코드로 디컴파일`
- `AndroidManifest.xml 및 리소스 추출`
- `디코드 및 디옵퓨스케이터 내장`: 난독화 된 코드 일부 자동 해독
- `GUI 및 CLI 모두 지원`
- `플러그인 시스템`

## 설치 방법
---
### GUI 버전
#### Windows
1. [JADX GitHub](https://github.com/skylot/jadx)에 접속하여 원하는 버전의 JADX 다운로드 후 압축 해제
	- 해당 파일의 이름에 win이 들어간 파일을 받아야 합니다.
2. 해당 폴더 내부의 `jadx-gui.exe`를 실행시킵니다.
#### mac
1. [JADX GitHub](https://github.com/skylot/jadx)에 접속하여 원하는 버전의 JADX 다운로드 후 압축 해제
	- 해당 파일의 이름에 win이 들어가지 않은 파일을 받아야 합니다.
2. 해당 폴더 내부의 `jadx-gui`를 실행합니다.

### CLI 버전
#### Linux
1. 컴파일 된 압축 파일 다운로드
```sh
# wget 명려어 또는 git 명령어 사용
wget https://github.com/skylot/jadx/releases/download/{version}}/jadx-{version}.zip
# or
git clone https://github.com/skylot/jadx.git
```

2. 압축 해제 후 실행 파일 실행
```
unzip jadx-{version}.zip
cd jadx-{version}

./bin/jadx sample.apk
```

#### mac
```sh
brew install jadx
```

## 간단 가이드
---
#### 실행 시 주의 사항
- JADX를 실행하기 위해서는 JAVA 11 이상이 설치되어 있어야 합니다.
- jre가 들어 있는 경우 추가로 JAVA를 설치 하지 않고도 실행이 가능합니다.

## 관련 URL
---
[JADX GitHub](https://github.com/skylot/jadx?tab=readme-ov-file)
