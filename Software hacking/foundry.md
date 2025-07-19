---
tags:
  - mac
  - windows
  - linux
  - web3
  - smart_contract
  - dev_tool
  - testing
---
## 설명
---
`Foundary`는 이더리움(Ethereum) 및 EVM 호환 블로체인 스마트 컨트랙트 개발을 위한 오픈소스 개발 툴체인 입니다. Rust 언어로 작성되어 있으며, 빠른 속도와 모듈성, 포터블한 설치 환경, 강력한 테스트 및 배포 기능으로 Web3 개발자들 사이에서 표준 도구로 자리 잡고 있습니다.

## 설치 영역
---
### Linux
`~/.foundary/bin/`

### mac
`~/.foundary`

## 주요 기능
---
- `스마트 컨트랙트 개발`: Solidity 기반 개발, Hardhat 보다 빠름
- `테스트 자동화`: Solidity로 직접 테스트 코드 작성 가능
- `배포`: forge script로 메인넷, 테스트넷 배포
- `온체인 데이터 조회`: cast로 블록체인 정보 조회 및 트랜잭션 실행
- `메인넷 포킹`: anvil로 로컬 환경에서 실전 테스트 가능
- `보안 테스트`: 퍼즈 테스트, 프라퍼티 기반 테스트 지원
- `개발 효율화`: 빠른 빌드, 배포 및 상호작용 지원

## 설치 방법
---
`Foundry`는 `foundryup` 스크립트를 통해 설치하는 것이 가장 일반적입니다.

### Linux / macOS
1.  터미널에서 다음 명령어를 실행하여 `foundryup`을 설치합니다.
    ```sh
    curl -L https://foundry.paradigm.xyz | bash
    ```
2.  설치 후 터미널을 다시 시작하거나, 다음 명령어를 실행하여 PATH 환경 변수를 업데이트합니다.
    ```sh
    source ~/.bashrc # 또는 ~/.zshrc
    ```

### Windows
1.  Windows에서는 `Git Bash` 또는 `WSL (Windows Subsystem for Linux)` 환경에서 설치하는 것을 권장합니다.
2.  `Git Bash` 또는 `WSL` 터미널을 열고, Linux/macOS와 동일하게 `curl -L https://foundry.paradigm.xyz | bash` 명령어를 실행합니다.

### 설치 시 주의 사항
- `foundryup`은 Foundry의 모든 도구(forge, cast, anvil, chisel)를 함께 설치합니다.
- 설치 후 `forge --version` 명령어를 통해 설치를 확인할 수 있습니다.

## 간단 가이드
---
1.  **새 프로젝트 생성**: `forge init` 명령어로 새로운 Foundry 프로젝트를 초기화합니다.
    ```sh
    forge init my-foundry-project
    cd my-foundry-project
    ```

2.  **스마트 컨트랙트 작성**: `src` 디렉토리에 Solidity 파일을 작성합니다. (예: `src/Counter.sol`)
    ```solidity
    // SPDX-License-Identifier: MIT
    pragma solidity ^0.8.18;

    contract Counter {
        uint public number;

        function setNumber(uint newNumber) public {
            number = newNumber;
        }

        function increment() public {
            number++;
        }
    }
    ```

3.  **컴파일**: `forge build` 명령어로 컨트랙트를 컴파일합니다.
    ```sh
    forge build
    ```

4.  **테스트 작성 및 실행**: `test` 디렉토리에 테스트 파일을 작성합니다. (예: `test/Counter.t.sol`)
    ```solidity
    // SPDX-License-Identifier: MIT
    pragma solidity ^0.8.18;

    import "forge-std/Test.sol";
    import "../src/Counter.sol";

    contract CounterTest is Test {
        Counter public counter;

        function setUp() public {
            counter = new Counter();
        }

        function testIncrement() public {
            counter.increment();
            assertEq(counter.number(), 1);
        }

        function testSetNumber() public {
            counter.setNumber(100);
            assertEq(counter.number(), 100);
        }
    }
    ```
    `forge test` 명령어로 테스트를 실행합니다.
    ```sh
    forge test
    ```

5.  **로컬 개발 블록체인 실행 (Anvil)**: `anvil` 명령어로 로컬 이더리움 블록체인을 실행합니다.
    ```sh
    anvil
    ```

6.  **컨트랙트 배포 (forge script)**: `script` 디렉토리에 배포 스크립트를 작성하고 `forge script`로 배포합니다.
    ```sh
    # 예시: script/DeployCounter.s.sol
    // SPDX-License-Identifier: MIT
    pragma solidity ^0.8.18;

    import "forge-std/Script.sol";
    import "../src/Counter.sol";

    contract DeployCounter is Script {
        function run() public returns (Counter) {
            vm.startBroadcast();
            Counter counter = new Counter();
            vm.stopBroadcast();
            return counter;
        }
    }
    ```
    ```sh
    forge script script/DeployCounter.s.sol --rpc-url http://127.0.0.1:8545 --private-key YOUR_PRIVATE_KEY --broadcast
    ```

7.  **블록체인 상호작용 (cast)**: `cast` 명령어로 블록체인과 상호작용합니다.
    ```sh
    # 현재 블록 번호 확인
    cast block-number

    # 특정 주소의 잔액 확인
    cast balance <ADDRESS>

    # 컨트랙트 함수 호출 (읽기 전용)
    cast call <CONTRACT_ADDRESS> "number()(uint256)"
    ```

## 관련 URL
---
[Solidity 웹사이트](https://soliditylang.org/)
[Foundry book](https://book.getfoundry.sh/)
[Foundry Book (Korean Ver.) by 허시원](https://dream-academy.gitbook.io/foundry-book-korean-ver.-by)
