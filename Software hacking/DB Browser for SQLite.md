---
tags:
  - mac
  - windows
  - linux
  - forensic
  - database
---
## 설명
---
`DB Browser for SQLite`는 SQLite 데이터베이스 파일을 쉽게 분석할 수 있도록 개발된 도구입니다.

## 설치 영역
---
`해당 프로그램은 portable파일을 지원함으로, 설치하지 않고 사용이 가능합니다.`

## 주요 기능
---
- 디지털 포렌식 분석
    - 모바일 기기의 SQLite DB 분석
    - 웹 브라우저 히스토리/캐시 조사
    - 메시징 앱 데이터베이스 분석

## 설치 방법
---
### Windows
1. [DB Browser for SQLite 웹사이트](https://sqlitebrowser.org/)에 접속하여 [Download](https://sqlitebrowser.org/dl/)탭에 들어갑니다.
2. 설치 파일 혹은 포터블 버전의 파일을 다운받습니다. 
	- 설치 버전은 .msi 파일을 실행시켜 설치를 진행하시면 됩니다.
	- Portable 버전은 다운 받은 파일을 압축해제하여 사용하시면 됩니다.

### mac
- Homebrew를 이용하여 설치할 수 있습니다.
```sh
brew install --cask db-browser-for-sqlite
```

## 간단 가이드
---
1.  **데이터베이스 열기**: `File > Open Database` 메뉴를 선택하거나, 툴바의 `Open Database` 아이콘을 클릭하여 분석할 SQLite 파일(확장자: `.db`, `.sqlite`, `.sqlite3` 등)을 엽니다.
2.  **데이터베이스 구조 확인**: `Database Structure` 탭에서 테이블, 인덱스, 뷰, 트리거의 목록과 각 테이블의 스키마(컬럼, 데이터 타입 등)를 확인할 수 있습니다.
3.  **데이터 조회**: `Browse Data` 탭을 선택하고, 드롭다운 메뉴에서 원하는 테이블을 선택하면 해당 테이블의 모든 데이터를 표 형태로 볼 수 있습니다.
4.  **SQL 쿼리 실행**: `Execute SQL` 탭으로 이동하여 직접 SQL 쿼리를 작성하고 실행할 수 있습니다. 상단의 쿼리 편집기에 쿼리를 입력하고 `Execute all/current SQL` (재생) 버튼을 누르면 하단에 결과가 표시됩니다.
5.  **데이터 수정**: `Browse Data` 탭에서 특정 셀을 더블클릭하여 직접 값을 수정하고 `Apply Changes` 버튼을 눌러 변경 사항을 저장할 수 있습니다. (주의: 원본 데이터가 변경되므로 신중하게 사용해야 합니다.)

### 사용 시 주의 사항
- SQLite의 DB만 사용이 가능합니다.

## 관련 URL
---
[DB Browser for SQLite 웹사이트](https://sqlitebrowser.org/)
[DB Browser for SQLite Download](https://sqlitebrowser.org/dl/)
