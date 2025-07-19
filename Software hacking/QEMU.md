---
tags:
  - windows
  - mac
  - linux
  - virtualization
  - emulation
  - pwnable
  - multi_platform
---
## 설명
---
`QEMU`는 오픈 소스 에뮬레이터이자 가상화 도구입니다. 다양한 하드웨어 아키텍처(x86, ARM, MIPS, PowerPC 등)를 에뮬레이션하여 한 시스템에서 다른 아키텍처용 소프트웨어를 실행할 수 있게 합니다. 또한, KVM(Kernel-based Virtual Machine)과 같은 하드웨어 가상화 기능을 활용하여 거의 네이티브에 가까운 성능으로 가상 머신을 실행할 수 있습니다.

## 설치 영역
---
### Windows
`C:\Program Files\qemu` (기본 설치 경로)

### mac
`/opt/homebrew/bin/qemu-system-x86_64` (Homebrew 설치 시)

### Linux
`/usr/bin/qemu-system-x86_64`

## 주요 기능
---
- `전체 시스템 에뮬레이션`: CPU, 메모리, 주변 장치 등 전체 시스템을 에뮬레이션하여 게스트 OS를 실행할 수 있습니다.
- `사용자 모드 에뮬레이션`: 다른 아키텍처용 바이너리를 현재 시스템에서 직접 실행할 수 있습니다.
- `하드웨어 가상화 지원`: KVM(Linux), Hypervisor.framework(macOS), HAXM(Windows) 등과 연동하여 가상 머신 성능을 향상시킵니다.
- `스냅샷`: 가상 머신의 특정 시점 상태를 저장하고 복원할 수 있습니다.
- `다양한 이미지 포맷 지원`: QCOW2, VMDK, VDI 등 다양한 가상 디스크 이미지 포맷을 지원합니다.

## 설치 방법
---
### Windows
1.  [QEMU 공식 웹사이트](https://www.qemu.org/download/#windows)에서 Windows용 설치 파일을 다운로드합니다.
2.  다운로드한 `qemu-w64-setup-*.exe` 파일을 실행하고 설치 마법사의 지시에 따라 설치를 진행합니다.
3.  설치 시 `Add QEMU to the system PATH` 옵션을 선택하면 명령 프롬프트에서 바로 QEMU 명령어를 사용할 수 있습니다.

### mac
1.  Homebrew를 사용하여 설치하는 것이 가장 편리합니다.
    ```sh
    brew install qemu
    ```

### Linux
1.  대부분의 리눅스 배포판에서 패키지 관리자를 통해 설치할 수 있습니다.
    ```sh
    # Debian/Ubuntu
    sudo apt update
    sudo apt install qemu-system-x86 qemu-utils

    # Fedora/CentOS
    sudo dnf install qemu-kvm qemu-img
    ```

## 간단 가이드
---
1.  **가상 디스크 이미지 생성**: QEMU에서 사용할 가상 디스크 이미지를 생성합니다.
    ```sh
    qemu-img create -f qcow2 my_linux.qcow2 20G
    ```
    *   `-f qcow2`: 이미지 포맷을 qcow2로 지정 (스냅샷, 동적 할당 등 지원)
    *   `my_linux.qcow2`: 생성할 이미지 파일 이름
    *   `20G`: 이미지 크기 (20GB)

2.  **가상 머신 실행**: ISO 파일을 사용하여 게스트 OS를 설치하거나, 이미 설치된 가상 디스크 이미지를 실행합니다.
    ```sh
    # ISO 파일로 설치 시작 (예: Ubuntu Server)
    qemu-system-x86_64 -m 2G -cpu host -smp 2 -hda my_linux.qcow2 -cdrom ubuntu-server.iso -boot d -enable-kvm

    # 설치된 가상 디스크 이미지 실행
    qemu-system-x86_64 -m 2G -cpu host -smp 2 -hda my_linux.qcow2 -enable-kvm
    ```
    *   `-m 2G`: 가상 머신에 2GB 메모리 할당
    *   `-cpu host`: 호스트 CPU와 동일한 CPU 사용 (성능 향상)
    *   `-smp 2`: 2개의 가상 CPU 코어 할당
    *   `-hda my_linux.qcow2`: 주 하드 디스크로 `my_linux.qcow2` 사용
    *   `-cdrom ubuntu-server.iso`: CD-ROM으로 `ubuntu-server.iso` 사용
    *   `-boot d`: CD-ROM으로 부팅
    *   `-enable-kvm`: KVM 가속 활성화 (리눅스 호스트에서만 사용 가능, 성능 향상)

3.  **네트워크 설정**: 기본적으로 NAT 모드로 설정되어 호스트의 네트워크를 공유합니다. 포트 포워딩을 설정하여 외부에서 게스트 OS에 접근할 수 있습니다.
    ```sh
    # 호스트의 8080 포트를 게스트의 80번 포트로 포워딩
    qemu-system-x86_64 ... -nic user,hostfwd=tcp::8080-:80
    ```

## 관련 URL
---
[QEMU 공식 웹사이트](https://www.qemu.org/)
[QEMU 위키](https://wiki.qemu.org/)
