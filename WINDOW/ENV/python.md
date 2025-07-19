# Windows에서 Python 사용하기

## 설명

이 문서는 Windows 운영체제에서 Python을 설치하고 사용하는 방법에 대한 기본적인 안내를 제공합니다. Python은 다양한 분야에서 사용되는 강력하고 유연한 프로그래밍 언어입니다.

## 설치 영역

`C:\Python` (기본 설치 경로, 버전 및 설정에 따라 달라질 수 있음)
`C:\Users\[사용자 이름]\AppData\Local\Programs\Python[버전]\Python.exe` (사용자별 설치 경로)
환경 변수 `PATH`에 Python 실행 파일 경로가 추가됩니다.

## 사용처

-   스크립트 작성 및 실행
-   웹 개발
-   데이터 분석 및 머신러닝
-   GUI 애플리케이션 개발
-   게임 개발
-   과학 및 공학 계산

## 설치(접속) 방법

1.  **Python 다운로드:**
    *   [Python 공식 웹사이트](https://www.python.org/downloads/windows/)에서 Windows용 Python 설치 파일을 다운로드합니다.  (최신 안정 버전 권장)
    *   "Windows installer (64-bit)" 또는 "Windows installer (32-bit)" 중 시스템에 맞는 것을 선택합니다.

2.  **Python 설치:**
    *   다운로드한 설치 파일을 실행합니다.
    *   **"Add Python 3.x to PATH"**  체크박스를 반드시 선택합니다. (매우 중요!)
        *   이 옵션을 선택하면 명령 프롬프트(cmd)나 PowerShell에서 `python` 명령어를 바로 사용할 수 있습니다.
    *   "Install Now"를 클릭하여 기본 설정으로 설치하거나, "Customize installation"을 선택하여 설치 경로 등을 변경할 수 있습니다.
    * 설치가 완료될 때까지 기다립니다.

## 접속 화면

*   명령 프롬프트(cmd) 또는 PowerShell을 엽니다.
    *   `python --version` 또는 `python -V` 를 입력하고 Enter 키를 누릅니다.
    *   설치된 Python 버전이 출력되면 설치가 성공적으로 완료된 것입니다.
    *   `pip --version` 또는 `pip -V`를 입력해서 pip (Python 패키지 관리자)도 잘 설치되었는지 확인합니다.

## 주의 사항

-   **PATH 환경 변수:**  "Add Python 3.x to PATH"를 선택하지 않으면, 명령 프롬프트에서 `python` 명령어를 사용할 수 없습니다.  이 경우 수동으로 PATH 환경 변수를 설정해야 합니다.
-   **여러 버전의 Python:**  여러 버전의 Python이 설치되어 있는 경우, `py` 런처를 사용하여 특정 버전을 실행할 수 있습니다. (예: `py -3.9`는 Python 3.9를 실행)
-   **권한 문제:**  특정 폴더에 Python 패키지를 설치하거나 파일을 생성할 때 권한 문제가 발생할 수 있습니다.  관리자 권한으로 명령 프롬프트 또는 PowerShell을 실행해야 할 수도 있습니다.
-   **Windows Store 버전 Python:** Windows Store에서 제공하는 Python은 일부 제약이 있을 수 있습니다. 공식 웹사이트에서 다운로드하는 것을 권장합니다.
- **가상환경:** 여러 프로젝트를 진행하는 경우, 각 프로젝트마다 독립적인 Python 환경을 구성하는 것이 좋습니다. `venv` 모듈을 사용하여 가상 환경을 생성하고 활성화할 수 있습니다.

## 관련 URL

-   [Python 공식 웹사이트](https://www.python.org/)
-   [Python Windows 다운로드 페이지](https://www.python.org/downloads/windows/)
-   [Python 3 Documentation (한국어)](https://docs.python.org/ko/3/)
-   [점프 투 파이썬 (Python 초보자를 위한 튜토리얼)](https://wikidocs.net/book/1)
-   [venv를 이용한 가상환경 설정](https://docs.python.org/ko/3/tutorial/venv.html)


