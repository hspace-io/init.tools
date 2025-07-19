# 해커 노트북 설정 가이드 (MacOS)

이 레포지토리는 Apple Silicon MacOS 컴퓨터에서 해킹 환경을 설정하기 위한 가이드입니다. 초보자 또는 다양한 해킹 도구를 효율적으로 탐색하려는 사용자를 위해 간단한 체크리스트를 통해 초기 설정 과정을 간소화하고 설정 관련 리소스를 줄이기 위해 제작되었습니다.

---

## 목적
이 가이드는 다음을 목표로 합니다:
- 초보 사용자가 필수 해킹 도구를 설치할 수 있도록 지원.
- 효율적인 설정을 위한 체크리스트 제공.
- 환경 수동 설정의 부담을 줄임.

---

## 추천 도구 분류 및 주요 기능

| 분류               | 도구명            | 기능                              | 권장 설치
|--------------------|------------------|----------------------------|--------------
| 시스템 및 개발 도구    | [Terminal](https://github.com/hspace-io/hacker-notebook-setup/tree/main/MAC/ENV/Terminal.md)            | 명령줄 인터페이스       |✅
| 시스템 및 개발 도구    | [Homebrew](https://github.com/hspace-io/hacker-notebook-setup/tree/main/MAC/ENV/Homebrew.md)         | 패키지 관리 도구.                 |✅
| 시스템 및 개발 도구    | [Visual Studio Code](https://github.com/hspace-io/hacker-notebook-setup/tree/main/MAC/ENV/VSCode.md) | 코드 편집기.                   |✅
| 시스템 및 개발 도구    | [C](https://github.com/hspace-io/hacker-notebook-setup/tree/main/MAC/ENV/C.md)                | 시스템 프로그래밍 언어.           |✅
| 시스템 및 개발 도구    | [Python](https://github.com/hspace-io/hacker-notebook-setup/tree/main/MAC/ENV/Python3.md)           | 범용 프로그래밍 언어.             |✅
| 시스템 및 개발 도구    | [Docker](https://github.com/hspace-io/hacker-notebook-setup/tree/main/MAC/ENV/Docker.md)           | 컨테이너 기반 가상화 도구.        |✅
| 시스템 및 개발 도구    | [OrbStack](https://github.com/hspace-io/hacker-notebook-setup/tree/main/MAC/ENV/OrbStack.md)        | 컨테이너 기반 가상화 도구.        |✅
| 시스템 및 개발 도구    | [UTM](https://github.com/hspace-io/hacker-notebook-setup/tree/main/MAC/ENV/UTM.md)              | 	가상화 소프트웨어 (ARM 기반 Mac 지원)                     |✅
| 시스템 및 개발 도구    | [VMware](https://github.com/hspace-io/hacker-notebook-setup/tree/main/MAC/ENV/VMware.md)           |	가상화 소프트웨어                    |
| 시스템 및 개발 도구    | [VirtualBox](https://github.com/hspace-io/hacker-notebook-setup/tree/main/MAC/ENV/VirtualBox.md)      | 	가상화 소프트웨어         |
| 네트워크 도구         | [NC](https://github.com/hspace-io/hacker-notebook-setup/tree/main/MAC/NET/NetCat.md)               | 	네트워크 연결 및 디버깅 도구                   | ✅
| 네트워크 도구         | [Shodan](https://github.com/hspace-io/hacker-notebook-setup/tree/main/MAC/NET/Shodan.md)           | 네트워크 장치 검색 도구.         | web | 
| 네트워크 도구         | [Censys](https://github.com/hspace-io/hacker-notebook-setup/tree/main/MAC/NET/Censys.md)           | 공개 네트워크 검색 도구.         | web | 
| 네트워크 도구         | [Nmap](https://github.com/hspace-io/hacker-notebook-setup/tree/main/MAC/NET/Nmap.md)             | 네트워크 포트 스캐너.            |
| 네트워크 도구         | [RustScan](https://github.com/hspace-io/hacker-notebook-setup/tree/main/MAC/NET/RustScan.md)         | 빠른 포트 스캐너.               |  
| 네트워크 도구         | [Wireshark](https://github.com/hspace-io/hacker-notebook-setup/tree/main/MAC/NET/Wireshark.md)        | 패킷 분석 도구.                | ✅
| 익스플로잇(PWN)      | GDB              | 디버깅 도구.                   |
| 익스플로잇(PWN)     | pwndbg            | LLDB, Gdb 확장 플러그인.       |
| 익스플로잇(PWN)     | [pwntools](https://github.com/hspace-io/hacker-notebook-setup/tree/main/MAC/PWN/pwntools.md)          | 익스플로잇 개발 라이브러리	           | ✅
| 익스플로잇(PWN)     | ROPGaget          |	ROP 체인 생성 도구                     |
| 익스플로잇(PWN)     | rp++              |ROP 체인 생성 도구 (고급)                      |
| 웹 테스트 도구      | [BurpSuite](https://github.com/hspace-io/hacker-notebook-setup/tree/main/MAC/WEB/BurpSuite.md)       | 웹 애플리케이션 테스트 도구.        |✅
| 웹 테스트 도구      | [OWASP_ZAP](https://github.com/hspace-io/hacker-notebook-setup/tree/main/MAC/WEB/OWASP_ZAP.md)       | 웹 애플리케이션 테스트 도구.        |
| 웹 테스트 도구      | [Fiddler](https://github.com/hspace-io/hacker-notebook-setup/tree/main/MAC/WEB/Fiddler.md)            | HTTP 트래픽 디버깅 도구.          |
| 웹 테스트 도구      | [CURL](https://github.com/hspace-io/hacker-notebook-setup/tree/main/MAC/WEB/CURL.md)             | 명령줄 기반 HTTP 요청 도구           |✅
| 웹 테스트 도구      | sqlmap           | 	SQL 인젝션 자동화 도구              |
| 암호화 도구         | [Sage](https://github.com/hspace-io/hacker-notebook-setup/tree/main/MAC/Crypto/Sage.md)             | 수학 및 암호화 라이브러리.        | ✅
| 암호화 도구         | [NumPy](https://github.com/hspace-io/hacker-notebook-setup/tree/main/MAC/Crypto/NumPy.md)            | 데이터 분석 라이브러리.           | ✅
| 암호화 도구         | [PyCryptodome](https://github.com/hspace-io/hacker-notebook-setup/tree/main/MAC/Crypto/PyCryptodome.md)     | 암호화 라이브러리.               | ✅
| 암호화 도구         | [CyberChef](https://github.com/hspace-io/hacker-notebook-setup/tree/main/MAC/Crypto/CyberChef.md)        | 데이터 변환 도구.               |✅
| 리버스 엔지니어링    | [IDA](https://github.com/hspace-io/hacker-notebook-setup/tree/main/MAC/REV/IDA.md)              | 바이너리 분석 도구.                | ✅
| 리버스 엔지니어링    | [Ghidra](https://github.com/hspace-io/hacker-notebook-setup/tree/main/MAC/REV/Ghidra.md)           | 리버스 엔지니어링 도구.             |
| 리버스 엔지니어링    | 010 Editor       | 바이너리 편집기.                  | 
| 리버스 엔지니어링    | wxMEdit          | 바이너리 편집기.                  | 
| 리버스 엔지니어링    | [Hex Fiend](https://github.com/hspace-io/hacker-notebook-setup/tree/main/MAC/REV/CheatEngine.md)        | 바이너리 편집기.                  | ✅
| 리버스 엔지니어링    | [Cheat Engine](https://github.com/hspace-io/hacker-notebook-setup/tree/main/MAC/REV/HexFiend.md)     | 메모리 에딧에 특화된 디버거.         | ✅
| 리버스 엔지니어링    | Frida            | 범용 후킹 프레임워크.               | 
| 리버스 엔지니어링    | z3               | SMT 솔버	                         |  
| 포렌식             | [Autopsy](https://github.com/hspace-io/hacker-notebook-setup/tree/main/MAC/Forensic/Autopsy.md)          | 파일 시스템 분석 도구.                     |
| 포렌식             | [Volatility](https://github.com/hspace-io/hacker-notebook-setup/tree/main/MAC/Forensic/Volatility.md)       | 메모리 분석 도구.                         |
| 블럭체인            | [Foundry](https://github.com/hspace-io/hacker-notebook-setup/tree/main/MAC/Blockchain/foundry.md) | 스마트 컨트랙트 개발 및 테스트 도구                                    | 
---
## 분야별 주의 사항
| 분야     | 주의사항            
|---------|------------------
| ENV     | 문제없음
| WEB     | 문제없음
| Crypto  | 문제없음
| NET     | 문제없음
| PWN     | UTM 같은 버츄얼 머신으로 원도우나 리눅스 에뮬레이터 돌려서 pwn 해킹이 가능함
| REV     | 정적분석은 가능, 동적 분석은 불가능
| FORensic| 불가능
---

## 참고 사항
- 문제 해결 및 고급 설정을 위해 문서의 상세 가이드를 참고하세요.
- 최신 도구와 실습 방법을 반영하기 위해 이 레포지토리는 지속적으로 업데이트됩니다.
