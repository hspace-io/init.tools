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
`JADX는 주로 압축 해제 후 실행하는 포터블 형태로 제공됩니다. 따라서 특정 고정된 설치 경로는 없습니다.`

## 주요 기능
---
- `DEX, APK, AAB, JAR, CLASS 등 다양한 파일을 Java 소스 코드로 디컴파일`
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
```sh
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
### GUI 사용법
1.  **APK/DEX 파일 열기**: `jadx-gui`를 실행하고 `File > Open file`을 선택하거나, 분석할 APK/DEX 파일을 JADX GUI 창으로 드래그 앤 드롭합니다.
2.  **디컴파일 진행**: 파일이 로드되면 JADX가 자동으로 디컴파일을 시작합니다. 이 과정은 파일 크기에 따라 시간이 걸릴 수 있습니다.
3.  **코드 탐색**: 왼쪽 패널의 트리 뷰에서 패키지, 클래스, 메서드 등을 탐색할 수 있습니다. 특정 클래스를 클릭하면 오른쪽 패널에 해당 클래스의 Java 소스 코드가 표시됩니다.
4.  **검색 기능**: `Search` 메뉴를 통해 클래스, 메서드, 필드, 문자열 등을 검색할 수 있습니다.
5.  **리소스 및 Manifest 확인**: `Resources` 탭에서 `AndroidManifest.xml` 파일과 기타 리소스 파일(레이아웃, 이미지 등)을 확인할 수 있습니다.

### CLI 사용법
1.  **기본 디컴파일**: APK 파일을 디컴파일하여 소스 코드를 특정 디렉토리에 저장합니다.
    ```sh
    jadx -d <출력 디렉토리> <APK 파일 경로>
    ```
    *   예시: `jadx -d output_dir my_app.apk`

2.  **디컴파일된 코드만 출력**: 소스 코드만 표준 출력으로 내보냅니다.
    ```sh
    jadx --show-bad-code <APK 파일 경로>
    ```

#### 실행 시 주의 사항
- JADX를 실행하기 위해서는 JAVA 11 이상이 설치되어 있어야 합니다.
- jre가 들어 있는 경우 추가로 JAVA를 설치 하지 않고도 실행이 가능합니다.

## 관련 URL
---
[JADX GitHub](https://github.com/skylot/jadx?tab=readme-ov-file)
