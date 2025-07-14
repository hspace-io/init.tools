---
tags:
  - windows
  - mac
  - network
  - packet_analysis
  - web_security
  - multi_platform
---
## 설명
---
`Wireshark`는 네트워크 프로토콜 분석기 (Network Protocol Analyzer) 또는 패킷 스니퍼(Packet Sniffer)라고 불리는 오픈소스 도구입니다. 실시간으로 네트워크 트래픽을 캡쳐하고, 캡쳐된 패킷 데이터를 사람이 읽기 쉬운 형태로 분석하여 보여줍니다. 네트워크 문제 해결, 보안 분석, 프로토콜 개발 및 교육 등 다양한 목적으로 사용됩니다.

## 설치 영역
---
### Windows
`C:\Program Files\Wireshark` (기본 설치 경로, 변경 가능)

### mac
`/Applications/Wireshark.app`

## 주요 기능
---
- `패킷 캡쳐 및 분석`: 실시간 네트워크 트래픽 캡쳐 또는 저장된 PCAP 파일 분석
- `프로토콜 지원`: TCP/IP, HTTP, DNS 등 수천 개의 네트워크 프로토콜 인식 및 분석
- `실시간 검사`: 네트워크 트래픽을 실시간으로 모니터링 하며 각 패킷의 상세 정보 표시
- `필터링 및 검색`: 특정 패킷, 세션, 프로토콜을 분리하여 분석할 수 있는 고급 필터 기능
- `그래픽 사용자 인터페이스`: 직관적인 GUI와 CLI (TShark) 모두 제공
- `시각화 도구`: 통계, 그래프, 플로우,다이어그램을 통한 네트워크 성능 시각화
- `프로토콜 분석`: 네트워크 프로토콜의 세부 동작 분석 및 헤더 정보 해석
- `VoIP 분석`: 캡쳐된 트래픽에서 VoIP 통화 감지 및 미디어 재생 기능
- `무선 네트워크 지원`: 무선 네트워크 인터페이스를 모니터 모드로 설정하여 분석

## 설치 방법
---
### Windows
1. Wireshark 다운로드: Wireshark 공식 웹사이트 ([https://www.wireshark.org/download.html](https://www.wireshark.org/download.html))에서 Windows용 설치 파일을 다운로드합니다. (일반적으로 "Windows Installer (64-bit)" 시스템에 맞는 것을 선택합니다.)
2. 설치 프로그램 실행: 다운로드한 설치 파일(예: Wireshark-win64-4.x.x.exe)을 실행합니다.
3. 설치 과정 진행:
    - 설치 마법사의 안내에 따라 설치를 진행합니다. 대부분의 경우 기본 설정을 유지해도 무방합니다.
    - **Npcap 설치:** Wireshark는 네트워크 패킷 캡처를 위해 Npcap (또는 WinPcap) 드라이버가 필요합니다.
    - **USBPcap 설치 (선택 사항):** USB 트래픽을 캡처하려면 USBPcap을 설치할 수 있습니다.
4. Wireshark 실행: 설치가 완료되면 시작 메뉴 또는 바탕 화면에서 Wireshark를 실행합니다.

### mac
- 아래 명령어를 터미널에 입력하여 설치 가능합니다.
```sh
brew install --caks wireshark
```

## 간단 가이드
---
### 사용 시 주의 사항
#### Windows
- 네트워크 트래픽을 캡쳐하려면 Wireshark를 관리자 권한으로 실행해야 하는 경우가 많습니다.
- Wireshark는 패킷 캡쳐를 위해 Npcap (또는 WinPcap)드라이버가 필요합니다. 설치 중에 함께 설치하거나,이미 설치되어 있는지 확인해야 합니다.
#### mac
- macOS에서는 네트워크 인터페이스 접근 제한이 있을 수 있으므로, 아래 명령으로 권한을 부여해야 합니다.
```sh
sudo chown {user_name} /dev/bpf*
```

## 관련 URL
---
[Wireshark 공식 웹사이트](https://www.wireshark.org/)
