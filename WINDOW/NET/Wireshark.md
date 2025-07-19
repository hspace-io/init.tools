# Wireshark (Windows)

## 설명
Wireshark는 네트워크 프로토콜 분석기(Network Protocol Analyzer) 또는 패킷 스니퍼(Packet Sniffer)라고 불리는 오픈 소스 도구입니다.  실시간으로 네트워크 트래픽을 캡처하고, 캡처된 패킷 데이터를 사람이 읽기 쉬운 형태로 분석하여 보여줍니다. 네트워크 문제 해결, 보안 분석, 프로토콜 개발 및 교육 등 다양한 목적으로 사용됩니다.

## 설치 영역
`C:\Program Files\Wireshark` (기본 설치 경로, 변경 가능)

## 사용처
- **네트워크 문제 해결**  
- **보안 분석**  
- **프로토콜 개발 및 디버깅**  
- **네트워크 교육**  
- **애플리케이션 분석**  

## 설치(접속) 방법
1. **Wireshark 다운로드:**  Wireshark 공식 웹사이트 ([https://www.wireshark.org/download.html](https://www.wireshark.org/download.html))에서 Windows용 설치 파일을 다운로드합니다.  (일반적으로 "Windows Installer (64-bit)" 시스템에 맞는 것을 선택합니다.)
2. **설치 프로그램 실행:** 다운로드한 설치 파일(예: Wireshark-win64-4.x.x.exe)을 실행합니다.
3. **설치 과정 진행:**
    *   설치 마법사의 안내에 따라 설치를 진행합니다.  대부분의 경우 기본 설정을 유지해도 무방합니다.
    *   **Npcap 설치:** Wireshark는 네트워크 패킷 캡처를 위해 Npcap (또는 WinPcap) 드라이버가 필요합니다.  
    *   **USBPcap 설치 (선택 사항):** USB 트래픽을 캡처하려면 USBPcap을 설치할 수 있습니다.  
4. **Wireshark 실행:** 설치가 완료되면 시작 메뉴 또는 바탕 화면에서 Wireshark를 실행합니다.
5. **관리자 권한 실행 (권장):** Wireshark를 사용하여 네트워크 인터페이스를 캡처하려면 일반적으로 관리자 권한으로 실행해야 합니다.  Wireshark 아이콘을 마우스 오른쪽 버튼으로 클릭하고 "관리자 권한으로 실행"을 선택합니다.

## 접속 화면
![Wireshark 초기 화면](wireshark_main_screen.png)




## 주의 사항
- **관리자 권한:** 네트워크 트래픽을 캡처하려면 Wireshark를 관리자 권한으로 실행해야 하는 경우가 많습니다.
- **Npcap (또는 WinPcap) 설치:**  Wireshark는 패킷 캡처를 위해 Npcap (또는 WinPcap) 드라이버가 필요합니다. 설치 중에 함께 설치하거나, 이미 설치되어 있는지 확인해야 합니다.


## 관련 URL
- **Wireshark 공식 웹사이트:** [https://www.wireshark.org/](https://www.wireshark.org/)
- **관련 블로그** [https://blog.naver.com/ds4ouj/222507823738](https://blog.naver.com/ds4ouj/222507823738)


