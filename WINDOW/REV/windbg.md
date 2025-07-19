# WinDbg (Windows Debugger)

## 설명
WinDbg는 Microsoft에서 제공하는 강력한 디버거로, Windows 운영 체제 및 응용 프로그램의 커널 모드 및 사용자 모드 디버깅을 모두 지원합니다.  주로 드라이버 개발, 시스템 문제 분석, 응용 프로그램 충돌 원인 파악, 악성코드 분석 등에 사용됩니다.  WinDbg (Preview) 버전은 기존 WinDbg의 현대적인 UI를 제공하는 버전입니다.

## 설치 영역
`C:\Program Files (x86)\Windows Kits\10\Debuggers\[x86|x64|arm64]` (SDK 설치 시 기본 경로)
`Microsoft Store` (WinDbg Preview 설치 시)

## 사용처
- **드라이버 개발 및 디버깅:**  커널 모드 드라이버의 동작을 단계별로 추적하고, 메모리 누수, 충돌 등의 문제를 해결합니다.
- **시스템 문제 분석:**  블루 스크린 (BSOD) 발생 시 덤프 파일을 분석하여 문제의 원인을 파악합니다. 시스템 행(hang) 문제 분석에도 활용됩니다.
- **응용 프로그램 디버깅:**  사용자 모드 응용 프로그램의 충돌, 예외 발생, 논리 오류 등을 디버깅합니다.
- **악성코드 분석:**  악성코드의 동작 방식을 분석하고, 시스템에 미치는 영향을 파악합니다.
- **리버스 엔지니어링:**  소프트웨어의 내부 동작 원리를 이해하고 분석합니다.

## 설치(접속) 방법
1. **Windows SDK 설치 (WinDbg):**
    -   Microsoft 웹사이트에서 최신 Windows SDK를 다운로드합니다.
    -   SDK 설치 과정에서 "Debugging Tools for Windows"를 선택합니다.
    -   설치가 완료되면, 설치 경로에서 `windbg.exe`를 실행합니다.
2. **Microsoft Store 설치 (WinDbg Preview):**
    -   Microsoft Store에서 "WinDbg Preview"를 검색하여 설치합니다.
    -   설치 후 시작 메뉴에서 "WinDbg Preview"를 실행합니다.

3. **디버깅 대상 연결:**
    - **로컬 커널 디버깅:**  `WinDbg`를 관리자 권한으로 실행하고, `File` -> `Kernel Debug` -> `Local` 탭에서 설정 후 `OK`를 클릭합니다. (시스템 재부팅 필요할 수 있음)
    - **원격 커널 디버깅:**  대상 컴퓨터에서 `bcdedit` 명령어를 사용하여 디버깅 설정을 구성하고, 호스트 컴퓨터의 `WinDbg`에서 `File` -> `Kernel Debug` -> 설정에 맞게 탭을 선택 후 연결합니다.
    - **사용자 모드 프로세스 연결 (Attach):**  `WinDbg`에서 `File` -> `Attach to a Process`를 선택하고, 디버깅할 프로세스를 선택합니다.
    - **사용자 모드 프로세스 실행 (Launch):** `WinDbg`에서 `File` -> `Open Executable`을 선택하고, 디버깅할 실행 파일을 선택합니다.
    - **덤프 파일 열기:** `WinDbg`에서 `File` -> `Open Crash Dump`를 선택하고, 덤프 파일 (.dmp)을 엽니다.

## 접속 화면
![WinDbg Preview 초기 화면](windbg_preview.png)
*(WinDbg Preview의 초기 화면 예시.  명령 창, 소스 코드 창, 메모리 창, 레지스터 창 등 다양한 창으로 구성됩니다.)*
![WinDbg 초기 화면](windbg.png)
*(WinDbg의 초기 화면 예시.  명령 창, 소스 코드 창, 메모리 창, 레지스터 창 등 다양한 창으로 구성됩니다.)*

## 주의 사항
- **관리자 권한:**  커널 디버깅 및 일부 사용자 모드 디버깅 작업에는 관리자 권한이 필요합니다.
- **심볼 파일 (Symbol Files):**  정확한 디버깅 정보를 얻으려면 Microsoft 심볼 서버 또는 로컬 심볼 경로를 올바르게 설정해야 합니다.  `File` -> `Symbol File Path` 에서 설정할 수 있습니다.  `.symfix` 명령어나 `.sympath` 명령어를 사용해서 설정할 수도 있습니다.
- **시스템 안정성:**  커널 디버깅 중에는 시스템이 불안정해지거나 충돌할 수 있으므로, 중요한 작업은 저장하고 진행하는 것이 좋습니다.  가상 머신 환경에서 디버깅하는 것을 권장합니다.
- **디버깅 대상 프로세스:**  디버깅 중인 프로세스는 중단되거나 느려질 수 있습니다.

## 관련 URL
[WinDbg 설명서 (Microsoft Docs)](https://docs.microsoft.com/en-us/windows-hardware/drivers/debugger/)
[WinDbg (Preview) 설명서](https://docs.microsoft.com/en-us/windows-hardware/drivers/debugger/debugger-download-tools)
[Windows SDK 다운로드](https://developer.microsoft.com/en-us/windows/downloads/windows-sdk/)
