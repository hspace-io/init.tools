## 설명
---
`Hardhat`은 이더리움 스마트 컨트랙트 개발, 테스트, 배포를 위한 유연하고 확장 가능한 개발 환경입니다. JavaScript/TypeScript 기반으로 작동하며, 개발자가 로컬에서 이더리움 네트워크를 시뮬레이션하고, 디버깅하며, 테스트를 자동화할 수 있도록 다양한 기능을 제공합니다.

## 설치 영역
---
`Hardhat`은 Node.js 패키지로 설치되므로, 프로젝트의 `node_modules` 디렉토리에 설치됩니다. 특정 고정된 시스템 경로는 없습니다.

## 주요 기능
---
- `로컬 이더리움 네트워크`: 개발 및 테스트를 위한 내장된 로컬 이더리움 네트워크(Hardhat Network) 제공
- `테스트 프레임워크`: Mocha, Chai와 같은 인기 있는 JavaScript 테스트 라이브러리와 통합
- `디버깅`: 트랜잭션 실행 흐름을 시각적으로 추적하고 변수 값을 확인할 수 있는 강력한 디버거
- `플러그인 시스템`: 다양한 기능을 추가할 수 있는 유연한 플러그인 아키텍처 (예: Ethers.js, Web3.js, Verify)
- `태스크 러너`: 사용자 정의 태스크를 생성하고 실행하여 개발 워크플로우 자동화
- `Solidity 컴파일러`: Solidity 코드를 컴파일하고 아티팩트(ABI, 바이트코드)를 생성

## 설치 방법
---
`Hardhat`은 npm(Node Package Manager)을 통해 프로젝트에 설치합니다.

1.  **Node.js 및 npm 설치**: 시스템에 Node.js와 npm이 설치되어 있어야 합니다.
2.  **새 프로젝트 생성**: 새로운 프로젝트 디렉토리를 만들고 해당 디렉토리로 이동합니다.
    ```sh
    mkdir my-hardhat-project
    cd my-hardhat-project
    ```
3.  **프로젝트 초기화**: `npm init -y` 명령어로 `package.json` 파일을 생성합니다.
    ```sh
    npm init -y
    ```
4.  **Hardhat 설치**: 프로젝트 디렉토리에서 다음 명령어를 실행하여 Hardhat을 개발 의존성으로 설치합니다.
    ```sh
    npm install --save-dev hardhat
    ```
5.  **Hardhat 프로젝트 초기화**: Hardhat 프로젝트를 초기화합니다.
    ```sh
    npx hardhat
    ```
    *   `Create a JavaScript project` 또는 `Create a TypeScript project`를 선택하고, `Create a .gitignore` 및 `Install hardhat-toolbox`를 선택하여 기본 설정을 완료합니다.

## 간단 가이드
---
1.  **컨트랙트 작성**: `contracts` 디렉토리에 Solidity 파일을 작성합니다. (예: `contracts/Greeter.sol`)
    ```solidity
    // SPDX-License-Identifier: UNLICENSED
    pragma solidity ^0.8.9;

    contract Greeter {
        string private _greeting;

        constructor(string memory _initialGreeting) {
            _greeting = _initialGreeting;
        }

        function greet() public view returns (string memory) {
            return _greeting;
        }

        function setGreeting(string memory _newGreeting) public {
            _greeting = _newGreeting;
        }
    }
    ```

2.  **컴파일**: `npx hardhat compile` 명령어로 컨트랙트를 컴파일합니다.
    ```sh
    npx hardhat compile
    ```

3.  **테스트 작성**: `test` 디렉토리에 JavaScript/TypeScript 테스트 파일을 작성합니다. (예: `test/Greeter.js`)
    ```javascript
    const { expect } = require("chai");
    const { ethers } = require("hardhat");

    describe("Greeter", function () {
        it("Should return the new greeting once it's changed", async function () {
            const Greeter = await ethers.getContractFactory("Greeter");
            const greeter = await Greeter.deploy("Hello, world!");
            await greeter.deployed();

            expect(await greeter.greet()).to.equal("Hello, world!");

            const setGreetingTx = await greeter.setGreeting("Hola, mundo!");

            // wait until the transaction is mined
            await setGreetingTx.wait();

            expect(await greeter.greet()).to.equal("Hola, mundo!");
        });
    });
    ```

4.  **테스트 실행**: `npx hardhat test` 명령어로 테스트를 실행합니다.
    ```sh
    npx hardhat test
    ```

5.  **로컬 네트워크 실행**: `npx hardhat node` 명령어로 로컬 개발 네트워크를 시작합니다.
    ```sh
    npx hardhat node
    ```

6.  **스크립트 실행**: `scripts` 디렉토리에 배포 또는 상호작용 스크립트를 작성하고 `npx hardhat run`으로 실행합니다. (예: `scripts/deploy.js`)
    ```javascript
    const hre = require("hardhat");

    async function main() {
        const Greeter = await hre.ethers.getContractFactory("Greeter");
        const greeter = await Greeter.deploy("Hello, Hardhat!");

        await greeter.deployed();

        console.log("Greeter deployed to:", greeter.address);
    }

    main()
        .then(() => process.exit(0))
        .catch((error) => {
            console.error(error);
            process.exit(1);
        });
    ```
    ```sh
    npx hardhat run scripts/deploy.js
    ```

## 관련 URL
---
[Hardhat 공식 문서](https://hardhat.org/docs)
[Hardhat GitHub](https://github.com/NomicFoundation/hardhat)
