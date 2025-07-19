---
tags:
  - windows
  - mac
  - linux
  - reverse_engineering
  - binary_analysis
  - debugging
  - pwnable
---
## 설명
---
`DIE (Detect It Easy)`는 실행 파일(EXE, DLL 등)의 파일 형식, 패커, 컴파일러 등을 자동 분석해 주는 경량 리버스 엔지니어링 도구 입니다.

## 설치 영역
---
`해당 프로그램은 portable파일을 지원함으로, 설치하지 않고 사용이 가능합니다.`

### Windows
- portable 버전만 존재

### mac
`/Applications/DiE.app`

## 주요 기능
---
- `패커/컴파일러 식별 (Signature 기반)`
	- UPX, Themida, VMProtect 등 다양한 패킹 도구 자동 탐지
	- 자체 시그니처 엔진 사용
- `멀티 플랫폼 파일 지원`
	- PE(Windows), ELF(Linux), Match-O(mac) 포맷 모두 분석 가능
- `파일 정보 상세 분석`
	- 기본적인 바이트/어셈블리 코드 확인 가능
- `스캔 결과 내보내기 및 자동화`
	- 분석 결과를 JSON, TXT 등으로 저장 가능
	- 커맨드 라인 사용 가능

## 설치 방법
---
### Windows
1. [Detect-It-Easy 깃허브](https://github.com/horsicq/Detect-It-Easy)에 접속하여 [Download release](https://github.com/horsicq/DIE-engine/releases)에서 해당하는 운영체제의 파일을 다운 받으시면 됩니다.
	- Windows 버전은 portable 버전만 존재하기에, 파일을 다운받아 압축해제하여 사용하시면 됩니다.

### mac
1. [Detect-It-Easy 깃허브](https://github.com/horsicq/Detect-It-Easy)에 접속하여 [Download release](https://github.com/horsicq/DIE-engine/releases)에서 해당하는 운영체제의 파일을 다운 받으시면 됩니다.
2. 다운 받은 파일을 실행 또는 압축 해제를 진행합니다.
	- Installer의 경우 실행하여 설치를 진행합니다.
	- portable 버전의 경우 압축해제하여 `Die.app`을 실행하여 사용하시면 됩니다.

## 간단 가이드
---
1.  **파일 열기**: DiE를 실행하고 분석할 파일을 창으로 드래그 앤 드롭하거나, `File > Open` 메뉴를 통해 파일을 엽니다.
2.  **기본 정보 확인**: 파일을 열면 자동으로 분석이 시작됩니다. 메인 화면에서는 파일 유형(예: PE, ELF), 아키텍처(32/64-bit), 컴파일러, 패커 정보 등을 요약해서 보여줍니다.
3.  **세부 정보 탭**: 왼쪽 패널에서 다양한 탭을 선택하여 상세 정보를 확인할 수 있습니다.
    *   `PE`/`ELF`/`Mach-O`: 파일 형식에 맞는 헤더 정보(섹션, 임포트/익스포트 테이블 등)를 보여줍니다.
    *   `Hex`: 파일의 내용을 16진수 뷰어로 보여줍니다.
    *   `Strings`: 파일 내에 포함된 문자열을 추출하여 보여줍니다.
    *   `Entropy`: 파일의 엔트로피를 시각적으로 분석하여 패킹 또는 암호화 여부를 추정하는 데 도움을 줍니다.
4.  **시그니처 스캔**: `Scan` 버튼을 누르면 DiE의 시그니처 데이터베이스를 기반으로 파일을 다시 스캔하여 더 정확한 정보를 찾아낼 수 있습니다.


## 관련 URL
---
[Detect-It-Easy 깃허브](https://github.com/horsicq/Detect-It-Easy)
[Detect-It-Easy Download release](https://github.com/horsicq/DIE-engine/releases)
