---
tags:
  - mac
  - linux
  - windows
  - reverse_engineering
  - pwnable
  - debugging
  - multi_platform
---
## 설명
---
`IDA Free`는 Hex-Rays에서 제공하는 무료 리버스 엔지니어링 도구로 상용 버전인 `IDA Pro`의 핵심 기능을 개인 및 비상업적 용도로 사용할 수 있도록 제공합니다.

## 설치 영역
---
### Windows
`C:\Program Files\IDA Freeware 7.x` (기본 설치 경로)

### mac
`/Applications/IDA Freeware 7.x/ida.app`

### Linux
`~/ida-freeware-7.x/ida` (설치 경로에 따라 다름)

## 주요 기능
---
- x86/x64 바이너리 디스어셈블
- 클라우드 기반 x64 디컴파일러
- 디버깅 기능 지원
- 데이터/코드 자동 분류, 함수, 그래프 등 시각화

## 설치 방법
---
1. [hex-rays 웹사이트](https://hex-rays.com/)에 접속해 `Products -> IDA Free`를 선택합니다.
2. 본인의 이메일을 입력하고, EULA에 동의하게 되면 IDA Free 라이센스가 발급 됩니다.
3. My Account를 눌러 로그인을 진행하게 되면 본인이 입력했던 이메일로 verification code가 전송됩니다. 해당 코드를 입력하여 로그인을 마무리 합니다.
4. 이후 My hex-rays에 Licenses에서 `Actions -> Download hexlic`으로 라이센스를 다운 받습니다.
5. 좌측의 메뉴에서 `Download center`메뉴를 선택하고, 원하는 버전을 선택한 다음 IDA Free를 선택합니다.
6. 보인의 환경에 맞는 설치 파일을 다운 받은 후 압축을 해제하고 설치 마법사를 따라 설치를 진행합니다.
7. IDA를 실행 시키면 라이센스가 등록이 되지 않았다고 나오게 되는데, 이때 다운 받은 hexlic를 찾아서 등록하게 된다면 사용 할 수 있게 됩니다.

## 간단 가이드
---
1.  **파일 열기**: IDA Free를 실행하고 `File > Open`을 선택하여 분석할 바이너리 파일을 엽니다. 또는 파일을 IDA Pro 아이콘으로 드래그 앤 드롭합니다.
2.  **분석 옵션 설정**: 파일을 열면 `Load new file` 대화 상자가 나타납니다. 대부분의 경우 기본 설정을 유지하고 `OK`를 클릭하여 분석을 시작합니다.
3.  **분석 진행**: IDA가 파일을 로드하고 자동 분석을 시작합니다. 이 과정은 파일 크기에 따라 시간이 걸릴 수 있습니다. 분석이 완료되면 `IDA View-A` 창에 디스어셈블된 코드가 표시됩니다.
4.  **디스어셈블된 코드 탐색**: `IDA View-A` 창에서 코드를 스크롤하거나, `Functions` 창(왼쪽)에서 특정 함수를 선택하여 해당 함수로 이동할 수 있습니다.
5.  **디컴파일된 코드 확인**: `Pseudocode-A` 창(보통 `IDA View-A` 옆에 위치)에서 현재 선택된 함수의 C언어 의사 코드(Pseudo-code)를 확인할 수 있습니다. 이는 바이너리 코드를 이해하기 쉽게 변환해 줍니다.
6.  **그래프 뷰**: `View > Graphs > Flow chart`를 선택하여 함수의 제어 흐름 그래프를 시각적으로 확인할 수 있습니다.
7.  **문자열 확인**: `View > Open subviews > Strings`를 선택하여 바이너리 내에 포함된 모든 문자열을 확인할 수 있습니다. 이는 중요한 정보나 메시지를 찾는 데 유용합니다.

### 사용 시 주의 사항
- 비상업적 용도에 한해 완전 무료입니다.

## 관련 URL
---
[IDA Free](https://hex-rays.com/ida-free)
