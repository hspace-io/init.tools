---
tags:
  - windows
  - forensic
  - disk_imaging
---
## 설명
---
디지털 증거 수집 및 이미징을 위한 포렌식 도구. 디스크 이미지 생성, 마운트, 파일 추출 등 다양한 포렌식 기능을 제공하는 전문 도구

## 설치 영역
---
### Windows
`C:\Program Files\AccessData\FTK Imager`

## 주요 기능
---
- 디지털 증거 수집
    - 디스크 이미징
    - 메모리 덤프 획득
    - 파일 시스템 분석
- 포렌식 분석
    - 삭제된 파일 복구
    - 파일 무결성 검증
    - 디스크 이미지 마운트
- 데이터 추출
    - 레지스트리 파일 추출
    - 암호화된 드라이브 분석
    - 특정 파일 유형 검색

## 설치 방법
---
1. [exterro 웹사이트](https://www.exterro.com/digital-forensics-software/ftk-imager)에서 FTK Imager 다운로드
2. 설치 파일 실행
3. 라이선스 동의 후 설치 진행
4. 시작 메뉴 또는 바탕화면 바로가기로 실행

## 간단 가이드
---
1.  **디스크 이미지 생성**:
    *   `File > Create Disk Image`를 선택합니다.
    *   증거 소스 유형(물리 디스크, 논리 드라이브 등)을 선택합니다.
    *   이미지를 저장할 대상 경로와 파일 이름, 이미지 형식(E01, DD 등)을 지정합니다.
    *   케이스 정보(조사관, 케이스 번호 등)를 입력하고 `Start`를 눌러 이미징을 시작합니다.

2.  **증거 파일 추가 및 탐색**:
    *   `File > Add Evidence Item`을 선택하여 분석할 이미지 파일이나 물리 디스크를 추가합니다.
    *   왼쪽 `Evidence Tree` 창에서 추가된 증거 항목을 탐색할 수 있습니다.

3.  **파일 미리보기 및 추출**:
    *   `File List` 창에서 파일을 선택하면 오른쪽 하단의 `View` 창에서 내용을 미리 볼 수 있습니다. (헥스, 텍스트, 그래픽 등)
    *   원하는 파일이나 폴더를 마우스 오른쪽 버튼으로 클릭하고 `Export Files`를 선택하여 PC로 추출할 수 있습니다.

4.  **메모리 캡처**:
    *   `File > Capture Memory`를 선택합니다.
    *   메모리 덤프를 저장할 경로를 지정하고 `Capture` 버튼을 누릅니다.

### 실행 시 주의 사항
- 관리자 권한으로 실행 필요
- 증거 수집 시 쓰기 방지 장치 사용 권장
- 이미징 시 충분한 저장 공간 확보 필요
- 메모리 덤프 시 시스템 리소스 많이 사용

## 관련 URL
---
[exterro 웹사이트](https://www.exterro.com/digital-forensics-software/ftk-imager)
