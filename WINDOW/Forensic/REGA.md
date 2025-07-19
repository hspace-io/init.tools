
# REGA

## 설명
REGA는 고려대학교 정보보호대학원의 디지털포렌식 연구실(DFRC)에서 제작한, 윈도우 레지스트리 수집 및 분석 도구입니다. REGA를 이용하여 쉽게 삭제된 레지스트리 Key와 Value를 확인가능하며, 레지스트리 키워드 검색 및 시간 검색 등 다양한 기능을 지원하며, 분석에 사용하는 파일은 다음 표와 같습니다.


| 파일 분류 | 파일명 | 위치 |
|---------|--------|------|
| **사용자 계정** |||
| Administrator | Administrator.NTUSER.DAT | C:\Users\Administrator |
| | Administrator.USRCLASS.DAT | C:\Users\Administrator |
| Default | Default User.NTUSER.DAT | C:\Users\Default |
| | Default.NTUSER.DAT | C:\Users\Default |
| %username% | %userprofile%.NTUSER.DAT | C:\Users\%username% |
| | %username%.USRCLASS.DAT | C:\Users\%username% |
| **시스템 구성** |||
| | COMPONENTS | C:\Windows\System32\config |
| | DEFAULT | C:\Windows\System32\config |
| | SECURITY | C:\Windows\System32\config |
| | SOFTWARE | C:\Windows\System32\config |
| | SYSTEM | C:\Windows\System32\config |
| **기타** |||
| | Amcache.hve | C:\Windows\appcompat\Programs |
| | RegEx.log | C:\Windows\System32\config |
| | SETUPAPI | C:\Windows\inf |
| | setupapi.dev.log | C:\Windows\inf |
| | SAM | C:\Windows\System32\config |


## 설치 영역
REGA는 설치형 애플리케이션이 아닌 압축된 파일로 제공되며, 사용자가 위치에 따라 설치할 수 있습니다.

## 사용처
* 레지스트리 분석
   * 레지스트리 하이브 파일 구조 분석 및 파싱
   * 시스템 설정 및 사용자 활동 내역 조사
   * 삭제된 레지스트리 키/값 복구 및 분석
* 디지털 포렌식 조사
   * 레지스트리 기반 아티팩트 수집 및 분석
   * 악성코드 관련 레지스트리 변조 흔적 탐지
   * 사용자 계정 활동 및 시스템 변경사항 추적
* 시스템 감사
   * 중요 레지스트리 키 변경 모니터링
   * 비인가 시스템 설정 변경 탐지
   * 자동 실행 프로그램 및 서비스 분석

## 설치(접속) 방법
1. **http://dfrc.korea.ac.kr/infra_dfrc_tools/?q=YToxOntzOjEyOiJrZXl3b3JkX3R5cGUiO3M6MzoiYWxsIjt9&bmode=view&idx=14616120&t=board 로 이동하여 도구를 다운로드.**
2. **REGA.exe를 실행하여 도구 사용.**

## 접속 화면
![image](https://github.com/user-attachments/assets/e2d05006-2ac0-484f-88ec-c10159e1134d)


## 주의 사항
- [주의사항 1: REGA를 로컬의 하이브가 아닌, 다른 컴퓨터를 대상으로 분석한다면, REGA 폴더 형식에 맡게 파일을 가져와야합니다.]
- 분석에 필요한 각 파일 위치는 [설명]과 같습니다.


## 관련 URL
[DFRC](http://dfrc.korea.ac.kr/infra_dfrc_tools/?q=YToxOntzOjEyOiJrZXl3b3JkX3R5cGUiO3M6MzoiYWxsIjt9&bmode=view&idx=14616120&t=board)
