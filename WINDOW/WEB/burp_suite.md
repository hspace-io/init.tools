# Burp Suite

## 설명
Burp Suite는 웹 애플리케이션의 보안 테스트를 위한 통합 플랫폼입니다. 웹 애플리케이션의 취약점을 찾고 공격하는 데 사용되는 다양한 도구를 제공합니다. PortSwigger 사에서 개발했습니다.

## 설치 영역
*   **Windows:** `.exe` 설치 파일 실행

## 사용처
- **웹 애플리케이션 취약점 분석:** 
- **HTTP/HTTPS 트래픽 가로채기 및 조작:**  
- **웹 애플리케이션 기능 테스트:**  

## 설치(접속) 방법
1. **다운로드:** PortSwigger 웹사이트([https://portswigger.net/burp/communitydownload](https://portswigger.net/burp/communitydownload))에서 Burp Suite Community Edition 다운로드합니다.
2. **설치:** 다운로드한 설치 파일을 실행하여 설치합니다. 
3. **실행:** Burp Suite를 실행합니다.  
4. **프록시 설정:** Burp Suite는 기본적으로 로컬 프록시(127.0.0.1:8080)를 사용합니다. 웹 브라우저의 프록시 설정을 Burp Suite 프록시로 설정합니다.
    *   **Firefox:** 설정 > 일반 > 네트워크 설정 > 설정... > 수동 프록시 구성 (HTTP 프록시: 127.0.0.1, 포트: 8080, "이 프록시 설정을 HTTPS에도 사용" 체크)
    *   **Chrome:** 설정 > 시스템 > 컴퓨터 프록시 설정 열기 > 수동 프록시 설정 (프록시 서버 사용 켬, 주소: 127.0.0.1, 포트: 8080)
5. **(선택 사항) 인증서 설치:** HTTPS 트래픽을 가로채기 위해서는 Burp Suite의 CA 인증서를 브라우저에 설치해야 합니다.
    *   Burp Suite에서 Proxy > Options > Proxy Listeners > Import / export CA certificate > Certificate in DER format > Next > 파일 저장
    *   브라우저의 인증서 관리자에서 "신뢰할 수 있는 루트 인증 기관"에 해당 인증서를 가져옵니다. (브라우저마다 방법이 다릅니다.)

## 접속 화면
![Burp Suite 대시보드](burp_suite_dashboard.png) 

## 주의 사항
- **Community Edition 제한:** Community Edition은 일부 기능이 제한됩니다 (예: 자동 스캔 기능).  모든 기능을 사용하려면 Professional Edition을 구매해야 합니다.
- **프록시 설정:** Burp Suite 사용을 마친 후에는 반드시 브라우저의 프록시 설정을 원래대로 되돌려야 합니다. 그렇지 않으면 인터넷 연결에 문제가 발생할 수 있습니다.


## 관련 URL
- **PortSwigger (Burp Suite 개발사):** [https://portswigger.net/](https://portswigger.net/)
- **Web Security Academy (PortSwigger에서 제공하는 웹 보안 학습 플랫폼):** [https://portswigger.net/web-security](https://portswigger.net/web-security)
