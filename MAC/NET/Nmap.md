# Nmap

## 설명
네트워크 포트 스캐너로, 열려 있는 포트 및 서비스를 확인할 수 있는 도구.

## 설치 영역
`/usr/local/bin/nmap`

## 사용처
- 네트워크 취약점 점검
- 서버 상태 파악

## 설치(접속) 방법
1. **Homebrew를 통해 설치:**
   ```bash
   brew install nmap
   ```
2. **설치 확인:**
   ```bash
   nmap --version
   ```

## 접속 화면
```
Nmap version 7.95 ( https://nmap.org )
Platform: arm-apple-darwin23.6.0
Compiled with: liblua-5.4.7 openssl-3.4.0 libssh2-1.11.1 libz-1.2.12 libpcre2-10.44 nmap-libpcap-1.10.4 nmap-libdnet-1.12 ipv6
Compiled without:
Available nsock engines: kqueue poll select
```

## 주의 사항
- Nmap 사용 시 네트워크 관리자와의 사전 협의가 필요합니다.

## 관련 URL
[Nmap 공식 웹사이트](https://nmap.org/)
