---
tags:
  - mac
  - windows
  - linux
  - network
  - cli_tool
  - debugging
  - port_scanner
  - multi_platform
---
## 설명
---
`netcat`은 TCP/IP 프로토콜을 사용하여 네트워크 연결을 통해 데이터를 읽고 쓰는 네트워크 유틸리티입니다.

## 설치 영역
---
### Windows
`C:\Program Files (x86)\Nmap\ncat.exe` (Nmap 설치 시)

### mac
`/usr/bin/nc` (기본 설치)

### Linux
`/usr/bin/nc`

## 주요 기능
---
- `TCP/UDP 연결생성 및 수신`: 클라이언트 서버 역할 모두 수행 가능
- 포트 스캐닝: 단일/범위 포트
- 파일 전송
- 포트 리스닝
- 네트워크 디버깅/진단

## 설치 방법
---
### Windows
1. [nmap 웹사이트](https://nmap.org/)에 접속해서 Nmap 환경에 맞는 설치 파일 다운로드
2. 설치 마법사에 따라 설치를 진행
	- `nmap-{version}-setup.exe` 실행
3. ncat 명령어를 이용해서 사용 가능
	- powershell에서 명령어(Ncat) 사용 가능합니다.

### Linux
- 아래의 명령어를 터미널에 입력하여 설치 할 수 있습니다.
```sh
sudo apt install netcat
```

### mac
- 기본적으로 설치 되어 있으나 필요시 homebrew를 이용해서 다운 가능
```sh
brew install netcat
```

## 간단 가이드
---
1.  **포트 스캔**: 특정 호스트의 열린 포트를 확인합니다.
    ```sh
    nc -zv <대상 IP> <시작 포트>-<끝 포트>
    ```
    *   예시: `nc -zv 192.168.1.1 1-1024` (1번부터 1024번 포트 스캔)

2.  **TCP 클라이언트**: 특정 포트로 TCP 연결을 시도하고 데이터를 주고받습니다.
    ```sh
    nc <대상 IP> <포트>
    ```
    *   예시: `nc example.com 80` (example.com의 80번 포트에 연결)

3.  **TCP 서버 (리스너)**: 특정 포트에서 들어오는 TCP 연결을 대기합니다.
    ```sh
    nc -lvp <포트>
    ```
    *   예시: `nc -lvp 1234` (1234번 포트에서 연결 대기)

4.  **파일 전송 (서버 -> 클라이언트)**:
    *   **서버 (파일 전송)**:
        ```sh
        nc -lvp 1234 < file_to_send.txt
        ```
    *   **클라이언트 (파일 수신)**:
        ```sh
        nc <서버 IP> 1234 > received_file.txt
        ```

5.  **간단한 HTTP 요청**: 웹 서버에 간단한 HTTP GET 요청을 보냅니다.
    ```sh
    (echo -e "GET / HTTP/1.0\r\n\r\n";) | nc example.com 80
    ```

#### 사용 시 주의 사항
- OS에 설치된 nc에 따라 옵션 사용 방법에 약간의 차이가 있을 수 있습니다.
- `netcat`은 강력한 도구이므로, 허가되지 않은 네트워크에서 사용 시 법적 문제가 발생할 수 있습니다.

## 관련 URL
---
[nmap 웹사이트](https://nmap.org/)
[Netcat (Wikipedia)](https://en.wikipedia.org/wiki/Netcat)
