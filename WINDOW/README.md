# 해커 노트북 설정 가이드 (WINDOW)
---

## 추천 도구 분류 및 주요 기능
| 분류               | 도구명            | 기능                              | 사용 가능 OS 
|--------------------|------------------|----------------------------|---------------------
| 시스템 및 개발 도구    | [Terminal](https://github.com/hspace-io/hacker-notebook-setup/blob/main/WINDOW/ENV/Terminal.md)                 | 명령줄 인터페이스       |✅
| 시스템 및 개발 도구    | [Visual Studio Code](https://github.com/hspace-io/hacker-notebook-setup/blob/main/WINDOW/ENV/VSCode.md) | 코드 편집기.                   |✅
| 시스템 및 개발 도구    | C                | 시스템 프로그래밍 언어.           | ✅
| 시스템 및 개발 도구    | [Python](https://github.com/hspace-io/hacker-notebook-setup/blob/main/WINDOW/ENV/python.md)           | 범용 프로그래밍 언어.             | ✅
| 시스템 및 개발 도구    | [Docker](https://github.com/hspace-io/hacker-notebook-setup/blob/main/WINDOW/ENV/Docker.md)           | 컨테이너 기반 가상화 도구.        | ✅
| 시스템 및 개발 도구    | [VMware](https://github.com/hspace-io/hacker-notebook-setup/blob/main/WINDOW/ENV/VMware.md)            |	가상화 소프트웨어                    |✅
| 시스템 및 개발 도구    | virtual box      | 	가상화 소프트웨어         |
| 시스템 및 개발 도구    | [WSL](https://github.com/hspace-io/hacker-notebook-setup/blob/main/WINDOW/ENV/wsl.md)              | 	Windows 전용 리눅스 서브시스템       | ✅
| 네트워크 도구         | [Shodan](https://github.com/hspace-io/hacker-notebook-setup/blob/main/WINDOW/NET/Shodan.md)           | 네트워크 장치 검색 도구.         | web | 
| 네트워크 도구         | [Censys](https://github.com/hspace-io/hacker-notebook-setup/blob/main/WINDOW/NET/Censys.md)           | 공개 네트워크 검색 도구.         | web | 
| 네트워크 도구         | Nmap             | 네트워크 포트 스캐너.            |  
| 네트워크 도구         | RustScan         | 빠른 포트 스캐너.               | 
| 네트워크 도구         | [Wireshark](https://github.com/hspace-io/hacker-notebook-setup/blob/main/WINDOW/NET/wireshark.md)        | 패킷 분석 도구.                | ✅
| 익스플로잇(PWN)      | GDB              | 디버깅 도구.                   |
| 익스플로잇(PWN)      | [gef](https://github.com/hspace-io/hacker-notebook-setup/blob/main/WINDOW/PWN/gef.md)              | 디버깅 도구.                   |  
| 익스플로잇(PWN)     | [pwntools](https://github.com/hspace-io/hacker-notebook-setup/blob/main/WINDOW/PWN/pwntools.md)          |익스플로잇 개발 라이브러리	                      | ✅
| 익스플로잇(PWN)     | ROPGaget          |	ROP 체인 생성 도구                     |  
| 익스플로잇(PWN)     | rp++              |ROP 체인 생성 도구 (고급)                      |  
| 웹 테스트 도구      | [Burp Suite](https://github.com/hspace-io/hacker-notebook-setup/blob/main/WINDOW/WEB/burp_suite.md)       | 웹 애플리케이션 테스트 도구.        |✅
| 웹 테스트 도구      | [Fiddler](https://github.com/hspace-io/hacker-notebook-setup/blob/main/WINDOW/WEB/Fiddler.md)          | HTTP 트래픽 디버깅 도구.          |✅
| 웹 테스트 도구      | [curl](https://github.com/hspace-io/hacker-notebook-setup/blob/main/WINDOW/WEB/curl.md)             | 명령줄 기반 HTTP 요청 도구                           |✅
| 웹 테스트 도구      | sqlmap           | 	SQL 인젝션 자동화 도구              |                 
| 웹 테스트 도구      | webhook          | 	웹훅 테스트 도구                               |web 
| 암호화 도구         | [NumPy](https://github.com/hspace-io/hacker-notebook-setup/blob/main/WINDOW/Crypto/Numpy.md)            | 데이터 분석 라이브러리.           | ✅
| 암호화 도구         | [PyCryptodome](https://github.com/hspace-io/hacker-notebook-setup/blob/main/WINDOW/Crypto/PyCryptodome.md)     | 암호화 라이브러리.               | ✅
| 암호화 도구         | [CyberChef](https://github.com/hspace-io/hacker-notebook-setup/blob/main/WINDOW/Crypto/CyberChef.md)        | 데이터 변환 도구.               |web | web
| 리버스 엔지니어링    | [IDA](https://github.com/hspace-io/hacker-notebook-setup/blob/main/WINDOW/REV/ida.md)              | 바이너리 분석 도구.                | ✅
| 리버스 엔지니어링    | Ghidra           | 리버스 엔지니어링 도구.             | 
| 리버스 엔지니어링    | 010 Editor       | 바이너리 편집기.                  |  
| 리버스 엔지니어링    | [HxD](https://github.com/hspace-io/hacker-notebook-setup/blob/main/WINDOW/REV/HxD.md)              | 바이너리 편집기.                  | ✅
| 리버스 엔지니어링    | wxMEdit          | 바이너리 편집기.                  |  
| 리버스 엔지니어링    | [Cheat Engine](https://github.com/hspace-io/hacker-notebook-setup/blob/main/WINDOW/REV/cheat_engine.md)     | 메모리 에딧에 특화된 디버거.         | ✅
| 리버스 엔지니어링    | dnSpy            | .NET 디컴파일러.                 |  
| 리버스 엔지니어링    | [x64dbg](https://github.com/hspace-io/hacker-notebook-setup/blob/main/WINDOW/REV/x64dbg.md)           | 오픈소스 윈도우 디버거.             | ✅
| 리버스 엔지니어링    | [windbg](https://github.com/hspace-io/hacker-notebook-setup/blob/main/WINDOW/REV/windbg.md)           | 윈도우 전용 디버거.                | ✅
| 리버스 엔지니어링    | Frida            | 범용 후킹 프레임워크.               |  
| 리버스 엔지니어링    | [z3](https://github.com/hspace-io/hacker-notebook-setup/blob/main/WINDOW/REV/z3.md)             | SMT 솔버	                         |  
| 포렌식             | Autopsy          | 파일 시스템 분석 도구.                     | 
| 포렌식             | [Volatility](https://github.com/hspace-io/hacker-notebook-setup/blob/main/WINDOW/Forensic/Volatility.md)      | 메모리 분석 도구.                         |✅
| 포렌식             | [BrowsingHistoryView](https://github.com/hspace-io/hacker-notebook-setup/blob/main/WINDOW/Forensic/BrowsingHistoryView.md)       | 브라우저의 사용 기록 분석 도구      |✅
| 포렌식             | [DB Browser for SQLite](https://github.com/hspace-io/hacker-notebook-setup/blob/main/WINDOW/Forensic/DB%20Browser%20for%20SQLite.md)       | SQLite DB 분석 도구.         |✅
| 포렌식             | [Encase](https://github.com/hspace-io/hacker-notebook-setup/blob/main/WINDOW/Forensic/EnCase.md)           | 파일 시스템 분석 도구 (유료)                | 
| 포렌식             | [FTK Imager](https://github.com/hspace-io/hacker-notebook-setup/blob/main/WINDOW/Forensic/FTK%20Imager.md)       | 파일 시스템 분석 도구                      |✅
| 포렌식             | [NTFS Log Tracker](https://github.com/hspace-io/hacker-notebook-setup/blob/main/WINDOW/Forensic/NTFS%20Log%20Tracker.md) | NTFS 파일 시스템 저널 분석 도구             |
| 포렌식             | [REGA](https://github.com/hspace-io/hacker-notebook-setup/tree/main/WINDOW/Forensic/REGA.md)     | 레지스트리 분석 도구.                      |✅
| 블럭체인            | Foundry | 스마트 컨트랙트 개발 및 테스트 도구                  |


---

## 참고 사항
- 문제 해결 및 고급 설정을 위해 문서의 상세 가이드를 참고하세요.
- 최신 도구와 실습 방법을 반영하기 위해 이 레포지토리는 지속적으로 업데이트됩니다.
