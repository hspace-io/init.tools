# CURL

## 설명
커맨드라인 기반의 데이터 전송 도구로, HTTP, FTP 등 다양한 프로토콜을 지원합니다.

## 설치 영역
`/usr/bin/curl`

## 사용처
- HTTP 요청 테스트
- API 호출 및 디버깅
- 파일 다운로드 및 업로드

## 설치(접속) 방법
1. **macOS 기본 설치됨 (설치 확인):**
   ```bash
   curl --version
   ```
2. **최신 버전이 필요할 경우 Homebrew로 설치:**
   ```bash
   brew install curl
   ```

## 접속 화면
```
curl 8.11.1 (arm64-apple-darwin20.0.0) libcurl/8.11.1 OpenSSL/3.0.15 (SecureTransport) zlib/1.2.13 zstd/1.5.6 libssh2/1.11.1 nghttp2/1.57.0
Release-Date: 2024-12-11
Protocols: dict file ftp ftps gopher gophers http https imap imaps ipfs ipns mqtt pop3 pop3s rtsp scp sftp smb smbs smtp smtps telnet tftp ws wss
Features: alt-svc AsynchDNS GSS-API HSTS HTTP2 HTTPS-proxy IPv6 Kerberos Largefile libz MultiSSL NTLM SPNEGO SSL threadsafe TLS-SRP UnixSockets zstd
```

## 주의 사항
- 네트워크 요청이 HTTPS로 전달될 경우, SSL 인증서 관련 설정이 필요할 수 있음.

## 관련 URL
[CURL 공식 웹사이트](https://curl.se/)
