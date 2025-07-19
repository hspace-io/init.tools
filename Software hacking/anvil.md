---
tags:
  - web3
  - smart_contract
  - blockchain
  - dev_tool
  - cli_tool
---
## 설명
---
`Anvil`은 Foundry 개발 도구 모음의 일부로, 로컬 이더리움 개발 블록체인입니다. 스마트 컨트랙트 개발 및 테스트를 위해 빠르고 안정적인 로컬 환경을 제공하며, 즉시 사용 가능한 계정, 사용자 정의 블록 생성, 트랜잭션 조작 등 다양한 기능을 지원합니다.

## 설치 영역
---
`Anvil`은 Foundry와 함께 설치되며, 일반적으로 시스템 PATH에 추가되어 어디서든 실행 가능합니다.

## 주요 기능
---
- `빠른 블록 생성`: 즉시 블록을 생성하여 트랜잭션 처리를 빠르게 테스트할 수 있습니다.
- `사용자 정의 계정`: 미리 생성된 10개의 테스트 계정과 함께, 원하는 수의 계정을 생성하고 잔액을 설정할 수 있습니다.
- `트랜잭션 조작`: 가스 가격, 블록 번호, 타임스탬프 등을 조작하여 특정 시나리오를 테스트할 수 있습니다.
- `포크 기능`: 실제 네트워크(Mainnet, Goerli 등)를 포크하여 실제 환경과 유사한 조건에서 테스트할 수 있습니다.
- `RPC 엔드포인트`: 표준 JSON-RPC 인터페이스를 제공하여 MetaMask, Web3.js, Ethers.js 등과 연동할 수 있습니다.
- `자동 채굴`: 트랜잭션이 발생할 때마다 자동으로 블록을 채굴합니다.

## 설치 방법
---
`Anvil`은 Foundry 도구 모음의 일부이므로, Foundry를 설치하면 함께 설치됩니다.

### Linux / macOS
1.  `foundryup` 스크립트를 사용하여 Foundry를 설치합니다.
    ```sh
    curl -L https://foundry.paradigm.xyz | bash
    ```
2.  설치 후 터미널을 다시 시작하거나 `source ~/.bashrc` (또는 `~/.zshrc`)를 실행하여 PATH를 업데이트합니다.

### Windows
1.  `PowerShell`을 관리자 권한으로 실행합니다.
2.  다음 명령어를 실행하여 `foundryup`을 설치합니다.
    ```powershell
    Invoke-Expression (New-Object Net.WebClient).DownloadString('https://foundry.paradigm.xyz/foundryup.ps1')
    ```

## 간단 가이드
---
1.  **Anvil 실행**: 터미널에서 `anvil` 명령어를 실행하면 로컬 이더리움 블록체인이 시작됩니다.
    ```sh
    anvil
    ```
    *   실행 시 10개의 테스트 계정 주소와 개인 키, 그리고 RPC 엔드포인트(기본값: `http://127.0.0.1:8545`)가 출력됩니다.

2.  **특정 포트에서 실행**: `-p` 또는 `--port` 옵션을 사용하여 원하는 포트에서 실행할 수 있습니다.
    ```sh
    anvil -p 8546
    ```

3.  **포크하여 실행**: `--fork-url` 옵션을 사용하여 실제 네트워크를 포크할 수 있습니다. (Infura, Alchemy 등 RPC URL 필요)
    ```sh
    anvil --fork-url https://mainnet.infura.io/v3/YOUR_INFURA_PROJECT_ID
    ```

4.  **MetaMask 연결**: Anvil이 실행되면 MetaMask와 같은 지갑을 `http://127.0.0.1:8545` (또는 지정한 포트)로 연결하여 테스트 계정을 가져오고 트랜잭션을 보낼 수 있습니다.

5.  **종료**: `Ctrl+C`를 눌러 Anvil을 종료합니다.

## 관련 URL
---
[Foundry Book (Anvil 문서)](https://book.getfoundry.sh/anvil/)
[Foundry GitHub](https://github.com/foundry-rs/foundry)
