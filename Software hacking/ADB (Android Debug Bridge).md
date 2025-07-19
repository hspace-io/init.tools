---
tags:
  - android
  - debugging
  - network
  - dev_tool
  - pwnable
  - mac
  - windows
---
## 설명
---
`ADB (Android Debug Bridge)`는 Google에서 제공하는 다목적 명령줄 도구로, 개발자가 Android 기기와 통신하고 디버깅 할 수 있도록 지원합니다. 앱 설치, 디버깅, 파일 전송, 시스템 로그 확인, 쉘 명령어 실행 등 다양한 기기 작업을 수행할 수 있으며, 클라이언트-서버 구조로 동잡합니다. 개발자뿐만 아니라 고급 사용자들이 Android 기기를 더 세밀하게 제어하고 관리하는데 필수적인 도구입니다.

## 설치 영역
---
### Windows
Android Studio를 통해 설치한 경우, 일반적으로 다음 경로에 위치합니다.
`C:\Users\<사용자 이름>\AppData\Local\Android\Sdk\platform-tools`

### mac
### homebrew로 설치한 경우
`/opt/homebrew/Caskroom/android-platform-tools/<버전>/platform-tools/adb`
### 설치 파일로 설치한 경우
`~/Library/Android/sdk/platform-tools`

## 주요 기능
---
- `앱 관리`: APK 파일 설치, 제거, 백업 및 복원
- `파일 전송`: 컴퓨터와 Android 기기 간 파일 복사 및 이동
- `시스템 디버깅`: 로그 캣 출력 확인, 시스템 로그 분석, 버그 리포트 생성
- `쉘 접근`: Unix 쉘을 통한 고급 명령 실행 및 시스템 제어
- `네트워크 연결`: USB 및 Wi-Fi를 통한 무선 디버깅 지원
- `루팅 지원`: 루팅 과정에서 필요한 명령 실행

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
brew install android-platform-tools
```

- [Android Studio 공식 웹사이트](https://developer.android.com/studio?hl=ko)를 통해서 설치하는 방법
	1. [Android Studio 공식 문서](https://developer.android.com/studio?hl=ko)에 설치 파일을 다운 받습니다.
	2. Android 스튜디오 DMG 파일을 시작합니다.
	3. Android 스튜디오를 Applications 폴더로 드래그한 다음 Android 스튜디오를 시작합니다.
	4. 이전 Android 스튜디오 설정을 가져올지 여부를 선택한 다음 **OK**를 클릭합니다.
	5. 개발에 필요한 Android SDK 구성요소를 다운로드하는 작업이 포함된 Android 스튜디오 **설정 마법사**를 완료합니다.

## 간단 가이드
---
1.  **기기 연결 확인**
    ```sh
    adb devices
    ```
    *   연결된 기기 목록과 상태(device, offline, unauthorized)를 확인합니다.
2.  **쉘 접속**
    ```sh
    adb shell
    ```
    *   Android 기기의 쉘 환경에 직접 접근하여 리눅스 명령어를 실행할 수 있습니다.
3.  **파일 전송**
    *   PC → 기기
        ```sh
        adb push <로컬 경로> <기기 경로>
        ```
    *   기기 → PC
        ```sh
        adb pull <기기 경로> <로컬 경로>
        ```
4.  **앱 설치 및 삭제**
    *   설치
        ```sh
        adb install <apk 파일 경로>
        ```
    *   삭제
        ```sh
        adb uninstall <패키지 이름>
        ```
5.  **로그 확인**
    ```sh
    adb logcat
    ```
    *   기기에서 발생하는 시스템 및 앱 로그를 실시간으로 출력합니다.


## 관련 URL
---
[Android Studio SDK 도구 가이드](https://developer.android.com/tools/releases/platform-tools?hl=ko)

