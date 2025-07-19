# NTFS Log Tracker

## 설명
NTFS Log Tracker는 $LogFile, $UsnJrnl:$J, $MFT 파일을 이용하여, NTFS 파일 시스템에서 발생하는 변경 사항을 추적하고 분석하는 포렌식 도구입니다.
이를 이용하여, 최근 삭제된 파일, 최근 변경된 파일, 최근 생성된 파일 등 다양한 이벤트를 확인할 수 있습니다.

## 설치 영역
해당 도구는, https://sites.google.com/site/forensicnote/ntfs-log-tracker 에서 무료로 배포되는 도구로, 사용자가 직접 압축을 해제하고 원하는 위치에 설치할 수 있습니다.

## 사용처
NTFS Log Tracker의 주요 사용처는 다음과 같습니다:

사용처:
* NTFS 파일 시스템 로그 분석
  - $LogFile 파싱을 통한 파일 시스템 변경 이력 확인
  - 삭제된 파일의 복구 및 시점 파악
  - 파일 시스템 메타데이터 분석

* 디지털 포렌식 조사
  - 사이버 침해사고 조사 시 파일 변경/삭제 흔적 분석
  - 악성코드에 의한 파일 시스템 변조 흔적 확인
  - 데이터 은닉/삭제 시도 탐지

## 설치(접속) 방법
1. **https://sites.google.com/site/forensicnote/ntfs-log-tracker에 접속하여, 다운로드 후 압축 해제하여 사용. **

## 접속 화면
![image](https://github.com/user-attachments/assets/1f7f74a9-56c3-4928-aee0-a04ff6aaecbf)

## 주의 사항
- [주의사항 1: NTFS Log Tracker를 사용하기 위해서는 FTK Imager 등으로 $MFT, $LogFile, $UsnJnl:$J파일을 export해야 사용 가능함.]

## 관련 URL
- [다운로드 링크](https://sites.google.com/site/forensicnote/ntfs-log-tracker)
- [NTFS 로그 분석을 통한 사용자 의심 행위 탐지에 관한 연구](https://www.kci.go.kr/kciportal/ci/sereArticleSearch/ciSereArtiView.kci?sereArticleSearchBean.artiId=ART002765136)
