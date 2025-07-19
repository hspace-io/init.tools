# 해커 노트북 설정 가이드
초보자 또는 다양한 해킹 도구를 효율적으로 탐색하려는 사용자를 위해 간단한 체크리스트를 통해 초기 설정 과정을 간소화하고 설정 관련 리소스를 줄이기 위해 제작되었습니다.

---

## 목적
이 가이드는 다음을 목표로 합니다:
- 초보 사용자가 필수 해킹 도구를 설치할 수 있도록 지원.
- 효율적인 설정을 위한 체크리스트 제공.

---
## 가이드
권장 설치은 지극히 HSPACE 해킹팀 knights 와 koreant의 의견입니다. 
|약자 | OS명| 진행사항 | 비고
|--|--|--|--
M | [macOS](https://github.com/hspace-io/hacker-notebook-setup/tree/main/MAC) | 32/42 |필수도구 완료 
W | [WINDOW](https://github.com/hspace-io/hacker-notebook-setup/tree/main/WINDOW)| 30/46 |필수도구 완료
L | [LINUX](https://github.com/hspace-io/hacker-notebook-setup/tree/main/LINUX) | 0/37|업데이트 중

---

## 추천 도구 분류 및 주요 기능

| 분류               | 도구명            | 기능                              | 사용 가능 OS | 권장 설치|
|--------------------|------------------|----------------------------|---------------------|--------
| 시스템 및 개발 도구    | Terminal            | 명령줄 인터페이스       |M W L | M W L
| 시스템 및 개발 도구    | Homebrew         | 패키지 관리 도구.                 |M L    | M
| 시스템 및 개발 도구    | Visual Studio Code | 코드 편집기.                   |M W L  | M W L
| 시스템 및 개발 도구    | C                | 시스템 프로그래밍 언어.           |M W L    | M W L
| 시스템 및 개발 도구    | Python           | 범용 프로그래밍 언어.             |M W L | M W L
| 시스템 및 개발 도구    | Docker           | 컨테이너 기반 가상화 도구.        |M W L | M W L
| 시스템 및 개발 도구    | Orb Stack        | 컨테이너 기반 가상화 도구.        |M  | M
| 시스템 및 개발 도구    | UTM              | 	가상화 소프트웨어 (ARM 기반 Mac 지원)                     |M  | M
| 시스템 및 개발 도구    | VMware           |	가상화 소프트웨어                    |M W | W
| 시스템 및 개발 도구    | virtual box      | 	가상화 소프트웨어         |M W L | 
| 시스템 및 개발 도구    | WSL              | 	Windows 전용 리눅스 서브시스템       | W | W
| 시스템 및 개발 도구    | virt-manager     | 	리눅스용 가상화 관리 도구       | L | L
| 네트워크 도구         | NC               | 	네트워크 연결 및 디버깅 도구                   | M L | M L
| 네트워크 도구         | Shodan           | 네트워크 장치 검색 도구.         | web | 
| 네트워크 도구         | Censys           | 공개 네트워크 검색 도구.         | web | 
| 네트워크 도구         | Nmap             | 네트워크 포트 스캐너.            | M W L | 
| 네트워크 도구         | RustScan         | 빠른 포트 스캐너.               | M W L | 
| 네트워크 도구         | Wireshark        | 패킷 분석 도구.                | M W L | M W L
| 익스플로잇(PWN)      | GDB              | 디버깅 도구.                   | M W L | L
| 익스플로잇(PWN)     | pwndbg            | LLDB, Gdb 확장 플러그인.       | M L | L
| 익스플로잇(PWN)     | gef               | Gdb 확장 플러그인.              | L | 
| 익스플로잇(PWN)     | pwntools          |익스플로잇 개발 라이브러리	                      | M W L | M W L
| 익스플로잇(PWN)     | ROPGaget          |	ROP 체인 생성 도구                     | M W L | L
| 익스플로잇(PWN)     | rp++              |ROP 체인 생성 도구 (고급)                      | M W L | L
| 웹 테스트 도구      | Burp Suite       | 웹 애플리케이션 테스트 도구.        |M W L | M W L
| 웹 테스트 도구      | Fiddler          | HTTP 트래픽 디버깅 도구.          |M W L | W
| 웹 테스트 도구      | CURL             | 명령줄 기반 HTTP 요청 도구                           |M W L | M W L
| 웹 테스트 도구      | sqlmap           | 	SQL 인젝션 자동화 도구              |M W L |                 
| 웹 테스트 도구      | webhook          | 	웹훅 테스트 도구                               |web | web
| 암호화 도구         | Sage             | 수학 및 암호화 라이브러리.        | M L | M L
| 암호화 도구         | NumPy            | 데이터 분석 라이브러리.           | M W L | M W L
| 암호화 도구         | PyCryptodome     | 암호화 라이브러리.               | M W L | M W L
| 암호화 도구         | CyberChef        | 데이터 변환 도구.               |web | web
| 리버스 엔지니어링    | IDA              | 바이너리 분석 도구.                | M W L  | M W L
| 리버스 엔지니어링    | Ghidra           | 리버스 엔지니어링 도구.             | M W L | 
| 리버스 엔지니어링    | 010 Editor       | 바이너리 편집기.                  | M W L | 
| 리버스 엔지니어링    | HxD              | 바이너리 편집기.                  | W     | W
| 리버스 엔지니어링    | wxMEdit          | 바이너리 편집기.                  | M W L | 
| 리버스 엔지니어링    | Hex Fiend        | 바이너리 편집기.                  | M     | M
| 리버스 엔지니어링    | Cheat Engine     | 메모리 에딧에 특화된 디버거.         | M W L | M W L
| 리버스 엔지니어링    | dnSpy            | .NET 디컴파일러.                 | W     | 
| 리버스 엔지니어링    | x64dbg           | 오픈소스 윈도우 디버거.             | W     | W
| 리버스 엔지니어링    | windbg           | 윈도우 전용 디버거.                | W     | W
| 리버스 엔지니어링    | Frida            | 범용 후킹 프레임워크.               | M W L | 
| 리버스 엔지니어링    | z3               | SMT 솔버	                         | M W L | 
| 포렌식             | Autopsy          | 파일 시스템 분석 도구.                     |M W |
| 포렌식             | Volatility       | 메모리 분석 도구.                         |M W | W
| 포렌식             | BrowsingHistoryView       | 브라우저의 사용 기록 분석 도구      |W |W
| 포렌식             | DB Browser for SQLite       | SQLite DB 분석 도구.         |W |W
| 포렌식             | Encase           | 파일 시스템 분석 도구 (유료)                |W
| 포렌식             | FTK Imager       | 파일 시스템 분석 도구                      |W | W
| 포렌식             | NTFS Log Tracker | NTFS 파일 시스템 저널 분석 도구             |W
| 포렌식             | REGA             | 레지스트리 분석 도구.                      |W | W
| 블럭체인            | Foundry | 스마트 컨트랙트 개발 및 테스트 도구                                    | M W L  | L


---

## 논란

| 분류               | 도구명            | 기능                              | 토론사유
|--------------------|------------------|----------------------------|---------------------
| 웹 테스트 도구        | DevTools       | 추후 토론 필요                 | 
| 파이썬 라이브러리      |request | 추후 토론 필요
| 익스플로잇(PWN)      | LLDB            | 추후 토론 필요               | 
| 익스플로잇(PWN)      | angr             | 추후 토론 필요                   | 


---

## 참고 사항
- 문제 해결 및 고급 설정을 위해 문서의 상세 가이드를 참고하세요.
- 최신 도구와 실습 방법을 반영하기 위해 이 레포지토리는 지속적으로 업데이트됩니다.
