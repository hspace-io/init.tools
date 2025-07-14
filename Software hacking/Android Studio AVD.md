---
tags:
  - mac
  - windows
  - linux
  - android
  - emulation
  - application
  - dev_tool
---
## 설명
---
`Android Stuio`는 Google에서 제공하는 Android를 앱 개발을 위한 공식 통합 개발 환경(IDE)입니다.

## 설치 영역
---
### Windows


### mac
`/Applications/Android Studio.app`

## 주요 기능
---
- `Gradle 기반 빌드 시스템`: 다양한 Android 기기 및 환경에 맞춘 빌드 커스터마이징과 성능 분석 지원
- `에뮬레이팅`: 다양한 Android 기기, 해상도, 버전에서 앱 테스트 가능
- `실시간 코드 편집`: 코드 변경 사항을 즉시 에뮬레이터/실기기에 반영
- `코드 템플릿 및 샘플 제공`: 빠른 프로젝트 생성과 표준 구조 제공
- `Lint 및 코드 분석 도구`: 성능, 보안, 호환성, 접근성 등 다양한 문제 자동 감지
- `C++ 및 네이티브 개발 지원`: NDK 통합, JNI 코드 작성 및 디버깅 가능
- `Git 등 버전 관리 시스템 연동`: 프로젝트 협업 및 소스 관리 지원
- `Google 서비스 통합`: FIrebase, Google Cloud, Wear OS, Android TV 등 다양한 플랫폼 지원
- `테스트 및 디버깅 도구`: JUnit, Espresso, UI Automator 등 자동화 테스트 프레임워크 내장

## 설치 방법
---
### Windows
- `EXE` 파일을 다운로드한 경우
	1. 파일을 더블클릭하여 실행합니다.

- `Zip` 파일을 다운로드한 경우:
    1. `Zip`의 압축을 풉니다.
    2. **android-studio** 폴더를 **Program Files** 폴더에 복사합니다.
    3. **android-studio > bin** 폴더를 엽니다.
    4. `studio64.exe`(64비트 컴퓨터) 또는 `studio.exe`(32비트 컴퓨터)를 실행합니다.
    5. Android 스튜디오의 **설정 마법사**에 따라 권장 SDK 패키지를 설치합니다.

### mac
- homebrew로 설치하는 방법은 아래의 명령어를 터미널에 입력하시면 됩니다.
```sh
# adb, fastboot 등의 도구가 함께 설치
brew install --cask android-studio
```

- [Android Studio 공식 웹사이트](https://developer.android.com/studio?hl=ko)를 통해서 설치하는 방법
	1. [Android Studio 공식 문서](https://developer.android.com/studio?hl=ko)에 설치 파일을 다운 받습니다.
	2. Android 스튜디오 DMG 파일을 시작합니다.
	3. Android 스튜디오를 Applications 폴더로 드래그한 다음 Android 스튜디오를 시작합니다.
	4. 이전 Android 스튜디오 설정을 가져올지 여부를 선택한 다음 **OK**를 클릭합니다.
	5. 개발에 필요한 Android SDK 구성요소를 다운로드하는 작업이 포함된 Android 스튜디오 **설정 마법사**를 완료합니다.

## 간단 가이드
---


## 관련 URL
---
[Android Studio 공식 웹사이트](https://developer.android.com/studio?hl=ko)