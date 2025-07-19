---
tags:
  - mac
  - windows
  - linux
  - debugging
  - pwnable
  - hooking
  - mobile
  - application
---
## 설명
---
Windows, macOS, Linux, IOS, Android, and QNX 기반의 네이트브 앱에 대해 후킹이 가능합니다. c로 개발되었지만, python을 이용하여 구현된 모듈이 존재합니다.

## 설치 영역
---
Frida는 Python 패키지로 설치되므로, 특정 경로에 설치되기보다는 Python의 `site-packages` 디렉토리에 설치됩니다. `frida-tools`의 실행 파일은 Python의 `Scripts` 또는 `bin` 디렉토리에 위치하게 됩니다.

## 주요 기능
---
- `함수 후킹`
- `동적 코드 삽입`
- `클래스 및 메서드 열람`
- `메모리 읽기/쓰기`
- `Anti-Debug / Anti-Root 우회`
- `스크립트 자동화 및 디버깅`
- `실시간 로그 출력 및 통신`

## 설치 방법
---
### Python 환경
1. 아래의 명령어를 터미널에 입력하여 설치 가능합니다.
```sh
pip install frida # PyPI 패키지
pip install frida-tools # cli 도구 모음
```

### 설치 시 주의 사항
- `pip install frida`는 Frida 엔진 및 API 기능을 제공합니다.
	- 주로 Python에서 import 하여 사용
	- 직접 JavaScript 후킹 스크립트를 실행하거나 연결할 때 사용
	- `frida`만 설치하고 싶은 경우 사용
- `pip install frida-tools`는 cli 도구 모음으로 아래의 도구들을 포함합니다.
	- `frida-trace`: 후킹 스크립트 자동 생성 및 트레이싱
	- `frida-ps`: 현재 실행 중인 프로세스 나열
	- `frida`: 기본적인 후킹 및 스크립트 실행
	- `frida-ls-devices`: 연결된 디바이스 나열

## 간단 가이드
---
1.  **실행 중인 프로세스 확인**: `frida-ps -Ua` 명령어로 USB로 연결된 모바일 기기에서 실행 중인 앱 목록을 확인합니다.
    ```sh
    frida-ps -Ua
    ```

2.  **특정 함수 트레이싱**: `frida-trace`를 사용하여 특정 앱의 함수 호출을 추적합니다. 예를 들어, `open` 함수를 트레이싱하고 싶을 때 사용합니다.
    ```sh
    # -U: USB 기기, -f: 앱 패키지 이름, -i: 포함할 함수
    frida-trace -U -f com.example.app -i "open"
    ```

3.  **JavaScript 스크립트로 후킹**: JavaScript 파일을 작성하여 특정 함수의 동작을 변경하거나 정보를 빼낼 수 있습니다.
    *   `hook.js` 파일 예시 (Java의 `MainActivity.secret` 함수의 리턴 값을 "Hello Frida!"로 변경)
        ```javascript
        Java.perform(function () {
            const MainActivity = Java.use('com.example.app.MainActivity');
            MainActivity.secret.implementation = function () {
                console.log('secret() is called');
                return 'Hello Frida!';
            };
        });
        ```
    *   스크립트 실행
        ```sh
        frida -U -f com.example.app -l hook.js
        ```

4.  **대화형 세션**: `-l` 옵션 없이 실행하면 Frida의 대화형 쉘에 진입하여 실시간으로 코드를 실행하고 분석할 수 있습니다.
    ```sh
    frida -U -f com.example.app
    ```

## 관련 URL
---
[Frida Github](https://github.com/frida/frida/releases)
[Frida Docs](https://frida.re/)