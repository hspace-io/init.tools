---
tags:
  - windows
  - mac
  - linux
  - scanning
  - network
  - cli_tool
  - multi_platform
  - port_scanner
---
## 설명
---
`RustScan`은 Rust로 작성된 초고속 포트 스캐너로, Nmap과 연동하여 빠른 포트 검색을 지원합니다.

## 설치 영역
---
`RustScan은 설치 방식에 따라 경로가 다를 수 있습니다. 일반적으로 시스템 PATH에 추가되어 어디서든 실행 가능합니다.`

## 주요 기능
---
- `초고속 포트 스캐닝`
- `스크립팅 엔진 지원`: Python, Lua, Shell 스크립트를 통한 자동화 및 확장 가능
- `Nmap 자동 연동`: 발견된 포트를 자동으로 Nmap으로 전달하여 상세 분석 수행
- `적응형 학습`: 사용자의 스캔 패턴을 학습하여 시간이 지날수록 성능 최적화
- `IPv6 및 CIDR 지원`: IPv4/IPv6 주소와 CIDR 표기법 지원
- `멀티 스레드 아키텍쳐`: 동시 다발적 스캔으로 속도 극대화

## 설치 방법
---
### Windows
1.  [RustScan GitHub Releases](https://github.com/RustScan/RustScan/releases) 페이지에서 최신 `rustscan-windows-x64.msi` 또는 `rustscan-windows-x64.zip` 파일을 다운로드합니다.
2.  `.msi` 파일의 경우 설치 마법사를 따라 설치를 진행합니다.
3.  `.zip` 파일의 경우 압축을 해제한 후, `rustscan.exe` 파일을 시스템 PATH에 추가하거나, 해당 디렉토리에서 직접 실행합니다.

### Linux
1.  [RustScan GitHub Releases](https://github.com/RustScan/RustScan/releases) 페이지에서 최신 `.deb` 또는 `.rpm` 파일을 다운로드합니다.
2.  `.deb` 파일의 경우:
    ```sh
    sudo dpkg -i rustscan_*.deb
    sudo apt install -f # 의존성 문제 해결
    ```
3.  `.rpm` 파일의 경우:
    ```sh
    sudo rpm -i rustscan_*.rpm
    ```
4.  또는 `cargo`를 통해 소스 코드에서 빌드할 수 있습니다. (Rust 설치 필요)
    ```sh
    cargo install rustscan
    ```

### mac
- 아래 명령어를 터미널에 입력하여 설치가 가능합니다.
```sh
brew install rustscan
```

## 간단 가이드
---
1.  **기본 스캔**: 대상 호스트의 모든 포트를 빠르게 스캔하고, 열린 포트를 Nmap으로 전달합니다.
    ```sh
    rustscan -a <대상 IP 주소 또는 도메인>
    ```
    *   예시: `rustscan -a 192.168.1.1` 또는 `rustscan -a example.com`

2.  **특정 포트 스캔**: 특정 포트만 스캔합니다.
    ```sh
    rustscan -a <대상> -p 22,80,443
    ```

3.  **Nmap 옵션 추가**: RustScan이 Nmap으로 전달할 추가 옵션을 지정합니다.
    ```sh
    rustscan -a <대상> -- -sV -O
    ```
    *   `--`: RustScan 옵션과 Nmap 옵션을 구분하는 구분자입니다.
    *   `-sV`: 서비스 버전 탐지
    *   `-O`: 운영체제 탐지

4.  **포트 범위 지정**: 스캔할 포트 범위를 지정합니다.
    ```sh
    rustscan -a <대상> --range 1-65535
    ```

5.  **속도 조절**: `--scan-mode` 옵션을 사용하여 스캔 속도를 조절할 수 있습니다. (예: `syn`, `connect`)
    ```sh
    rustscan -a <대상> --scan-mode syn
    ```

### 사용 시 주의 사항
- RustScan은 Nmap과 함께 사용해야 더 강력한 기능을 발휘합니다.
- 대량의 포트를 빠르게 스캔하므로, 대상 시스템에 부하를 줄 수 있습니다. 허가된 환경에서만 사용해야 합니다.

## 관련 URL
---
[RustScan 공식 웹사이트](https://rustscan.github.io/RustScan/)
[RustScan GitHub](https://github.com/RustScan/RustScan)
