---
tags:
  - windows
  - forensic
  - artifact_analysis
  - registry_analysis
---
## 설명
---
`REGA`는 고려대학교 정보보호 대학원의 디지털포렌식(DFRC)에서 제작한, 윈도우 레지스트리 수집 및 분석 도구입니다. REGA를 잉요하여 쉽게 삭제된 레지스트리 KEY와 Value를 확인가능하며, 레지스트리 키워드 검색 및 시간 검색 등 다양한 기능을 지원합니다. 

## 설치 영역
---
REGA는 설치형 애플리케이션이 아닌 압축된 파일로 제공되며, 사용자가 위치에 따라 설치할 수 있습니다.

## 주요 기능
---
- `레지스트리 수집`
	- 현재 시스템 레지스트리 실시간 수집
	- 복원지접 레지스트리 수집 지원
	- 하이브 파일(SAM, SYSTEM, SOFTWARE, SECURITY, NTUSER.DAT 등) 자동 추출
- `레지스트리 분석`
	- 레지스트리 하이브 파일 구조 분석 및 파싱
	- 시스템 설정 및 사용자 활동 내역 조사
	- 삭제된 레지스트리 키/값 복구 및 분석
- `디지털 포렌식 조사`
	- 레지스트리 기반 아티팩트 수집 및 분석
	- 악성코드 관련 레지스트리 변조 흔적 탐지
	- 사용자 게정 활동 및 시스템 변경사항 추적
- `사용자 계정 활동 및 시스템 변경사항 추적`
	- 중요 레지스트리 키 변경 모니터링
	- 비인가 시스템 설정 변경 탐지
	- 자동 실행 프로그램 및 서비스 분석

## 설치 방법
---
- [REGA 공식 웹사이트](https://dfrc.korea.ac.kr/infra_dfrc_tools/?q=YToxOntzOjEyOiJrZXl3b3JkX3R5cGUiO3M6MzoiYWxsIjt9&bmode=view&idx=14616120&t=board)에 접속하여 도구를 다운로드 합니다.
- 파일의 압축을 해제한 뒤 REGA.exe를 실행하여 도구를 사용하시면 됩니다.

## 간단 가이드
---
- 분석에 사용하는 파일은 다음 표와 같습니다.

| 파일 분류         | 파일명                        | 위치                            |
| ------------- | -------------------------- | ----------------------------- |
| **사용자 계정**    |                            |                               |
| Administrator | Administrator.NTUSER.DAT   | C:\Users\Administrator        |
|               | Administrator.USRCLASS.DAT | C:\Users\Administrator        |
| Default       | Default User.NTUSER.DAT    | C:\Users\Default              |
|               | Default.NTUSER.DAT         | C:\Users\Default              |
| %username%    | %userprofile%.NTUSER.DAT   | C:\Users%username%            |
|               | %username%.USRCLASS.DAT    | C:\Users%username%            |
| **시스템 구성**    |                            |                               |
|               | COMPONENTS                 | C:\Windows\System32\config    |
|               | DEFAULT                    | C:\Windows\System32\config    |
|               | SECURITY                   | C:\Windows\System32\config    |
|               | SOFTWARE                   | C:\Windows\System32\config    |
|               | SYSTEM                     | C:\Windows\System32\config    |
| **기타**        |                            |                               |
|               | Amcache.hve                | C:\Windows\appcompat\Programs |
|               | RegEx.log                  | C:\Windows\System32\config    |
|               | SETUPAPI                   | C:\Windows\inf                |
|               | setupapi.dev.log           | C:\Windows\inf                |
|               | SAM                        | C:\Windows\System32\config    |

### 사용 시 주의 사항
- REGA를 로컬의 하이브가 아닌, 다른 컴퓨터를 대상으로 분석한다면, REGA 폴더 형식에 맞게 파일을 파일을 가져와야 합니다.

## 관련 URL
---
[REGA 공식 웹사이트](https://dfrc.korea.ac.kr/infra_dfrc_tools/?q=YToxOntzOjEyOiJrZXl3b3JkX3R5cGUiO3M6MzoiYWxsIjt9&bmode=view&idx=14616120&t=board)
