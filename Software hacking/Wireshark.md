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
1.  **인터페이스 선택 및 캡처 시작**: Wireshark를 실행하면 사용 가능한 네트워크 인터페이스 목록이 나타납니다. 트래픽을 캡처할 인터페이스(예: Wi-Fi, 이더넷)를 선택하고 더블클릭하거나, 상단의 `Start capturing packets` (상어 지느러미 아이콘) 버튼을 클릭합니다.

2.  **패킷 목록 분석**: 캡처가 시작되면 실시간으로 패킷 목록이 표시됩니다. 각 패킷은 번호, 시간, 출발지/목적지 IP, 프로토콜, 길이, 정보 등으로 구성됩니다.

3.  **패킷 상세 정보 확인**: 패킷 목록에서 특정 패킷을 클릭하면, 아래 세 개의 패널에서 상세 정보를 확인할 수 있습니다.
    *   **Packet Details**: 선택된 패킷의 프로토콜 계층별 상세 정보(이더넷, IP, TCP/UDP, HTTP 등)를 트리 형태로 보여줍니다.
    *   **Packet Bytes**: 선택된 패킷의 원시 바이트 데이터를 16진수 및 ASCII 형태로 보여줍니다.

4.  **필터 사용**: 특정 패킷만 보고 싶을 때 필터를 사용합니다. Wireshark 상단의 `Apply a display filter` 입력란에 필터 규칙을 입력하고 `Apply` (오른쪽 화살표) 버튼을 클릭합니다.
    *   예시:
        *   `http`: HTTP 프로토콜 패킷만 표시
        *   `tcp.port == 80`: 80번 포트를 사용하는 TCP 패킷만 표시
        *   `ip.addr == 192.168.1.1`: 특정 IP 주소와 관련된 패킷만 표시
        *   `http.request.method == "POST"`: POST 요청만 표시

5.  **패킷 저장 및 열기**: 캡처된 패킷은 `File > Save` 또는 `File > Save As`를 통해 `.pcap` 또는 `.pcapng` 형식으로 저장할 수 있습니다. 저장된 파일은 `File > Open`을 통해 다시 불러와 분석할 수 있습니다.

6.  **통계 분석**: `Statistics` 메뉴를 통해 프로토콜 계층별 통계, 대화(Conversations), 엔드포인트(Endpoints) 등 다양한 네트워크 통계를 확인할 수 있습니다.

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
