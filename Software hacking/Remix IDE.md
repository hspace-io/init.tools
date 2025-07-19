---
tags:
  - web3
  - smart_contract
  - dev_tool
---
## 설명
---
`Remix IDE`는 이더리움 스마트 컨트랙트 개발을 위한 강력한 웹 기반 통합 개발 환경(IDE)입니다. Solidity 언어로 스마트 컨트랙트를 작성, 컴파일, 배포 및 디버깅하는 데 필요한 모든 기능을 제공하며, 로컬 환경 설정 없이 웹 브라우저에서 바로 사용할 수 있다는 장점이 있습니다.

## 설치 영역
---
`Remix IDE는 웹 기반 도구이므로 별도의 설치가 필요 없습니다. 웹 브라우저를 통해 접속하여 사용합니다.`

## 주요 기능
---
- `Solidity 코드 편집기`: 구문 강조, 자동 완성, 오류 검사 등 편리한 코드 작성 기능 제공
- `컴파일러`: Solidity 컴파일러를 내장하여 스마트 컨트랙트 코드를 바이트코드 및 ABI로 컴파일
- `배포 및 실행`: JavaScript VM, Injected Provider (MetaMask), Web3 Provider (Ganache, Geth 등)를 통해 다양한 환경에 스마트 컨트랙트 배포 및 함수 호출 가능
- `디버거`: 배포된 스마트 컨트랙트의 트랜잭션을 단계별로 디버깅하여 문제 해결 지원
- `테스트`: 내장된 테스트 프레임워크를 통해 스마트 컨트랙트의 단위 테스트 작성 및 실행
- `플러그인 시스템`: 다양한 추가 기능을 플러그인 형태로 제공 (예: Slither, LearnEth)

## 설치 방법
---
Remix IDE는 웹 기반 도구이므로 별도의 설치 과정이 필요 없습니다. 웹 브라우저를 통해 다음 URL에 접속하여 바로 사용할 수 있습니다.

1.  [Remix IDE 공식 웹사이트](https://remix.ethereum.org/)에 접속합니다.

## 간단 가이드
---
1.  **새 파일 생성**: Remix IDE에 접속하면 왼쪽 `File Explorers` 패널에서 `contracts` 폴더를 클릭하고 `Create New File` 아이콘을 클릭하여 새 Solidity 파일을 생성합니다. (예: `MyContract.sol`)

2.  **스마트 컨트랙트 작성**: 생성된 파일에 Solidity 코드를 작성합니다.
    ```solidity
    // SPDX-License-Identifier: GPL-3.0
    pragma solidity >=0.7.0 <0.9.0;

    contract MyContract {
        string public greeting;

        constructor() {
            greeting = "Hello, Remix!";
        }

        function setGreeting(string memory _greeting) public {
            greeting = _greeting;
        }
    }
    ```

3.  **컴파일**: 왼쪽 패널에서 `Solidity Compiler` 아이콘(솔리디티 로고)을 클릭합니다. `Compiler` 버전이 코드의 `pragma`와 일치하는지 확인하고 `Compile MyContract.sol` 버튼을 클릭합니다. 컴파일에 성공하면 녹색 체크 표시가 나타납니다.

4.  **배포 및 실행**: 왼쪽 패널에서 `Deploy & Run Transactions` 아이콘(이더리움 로고)을 클릭합니다.
    *   `Environment`: `JavaScript VM`을 선택합니다. (테스트용 가상 블록체인 환경)
    *   `Account`: 기본 계정 중 하나를 선택합니다.
    *   `Contract`: 드롭다운에서 `MyContract`를 선택합니다.
    *   `Deploy` 버튼을 클릭하여 스마트 컨트랙트를 배포합니다.

5.  **배포된 컨트랙트 상호작용**: 배포가 성공하면 `Deployed Contracts` 섹션에 `MYCONTRACT` 인스턴스가 나타납니다. 여기에서 컨트랙트의 함수를 호출할 수 있습니다.
    *   `greeting` 버튼을 클릭하여 현재 `greeting` 값을 확인합니다.
    *   `setGreeting` 옆의 입력란에 새로운 문자열을 입력하고 `setGreeting` 버튼을 클릭하여 값을 변경합니다.
    *   다시 `greeting` 버튼을 클릭하여 변경된 값을 확인합니다.

## 관련 URL
---
[Remix IDE 공식 웹사이트](https://remix.ethereum.org/)
[Solidity 공식 문서](https://docs.soliditylang.org/)
