## 설명
---
`Ethers.js`는 이더리움 블록체인과 상호작용하기 위한 강력하고 경량화된 JavaScript 라이브러리입니다. 웹 애플리케이션(프론트엔드) 및 Node.js 환경(백엔드)에서 이더리움 지갑 관리, 트랜잭션 전송, 스마트 컨트랙트 상호작용, 블록체인 데이터 조회 등 다양한 작업을 수행할 수 있도록 설계되었습니다.

## 설치 영역
---
`Ethers.js`는 JavaScript 라이브러리이므로, 프로젝트의 `node_modules` 디렉토리에 설치됩니다. 특정 고정된 시스템 경로는 없습니다.

## 주요 기능
---
- `지갑 관리`: 이더리움 지갑 생성, 가져오기, 서명, 트랜잭션 전송 등
- `Provider`: 이더리움 네트워크(Mainnet, Testnet, 로컬 노드 등)에 연결하여 블록체인 데이터 조회
- `Contract`: 스마트 컨트랙트의 ABI(Application Binary Interface)를 사용하여 컨트랙트 함수 호출 및 이벤트 수신
- `유틸리티`: 이더리움 주소 유효성 검사, 해시 함수, 단위 변환(wei, ether) 등 다양한 유틸리티 함수 제공
- `ENS (Ethereum Name Service)`: 도메인 이름을 이더리움 주소로 변환하거나 그 반대로 변환

## 설치 방법
---
`Ethers.js`는 npm(Node Package Manager)을 통해 프로젝트에 설치합니다.

1.  **Node.js 및 npm 설치**: 시스템에 Node.js와 npm이 설치되어 있어야 합니다.
2.  **프로젝트 초기화 (선택 사항)**: 새 프로젝트에서 시작하는 경우 `npm init -y` 명령어로 `package.json` 파일을 생성합니다.
3.  **Ethers.js 설치**: 프로젝트 디렉토리에서 다음 명령어를 실행합니다.
    ```sh
    npm install ethers
    ```
    또는 `yarn`을 사용하는 경우:
    ```sh
    yarn add ethers
    ```

## 간단 가이드
---
### 1. Provider를 사용하여 블록체인 데이터 조회
```javascript
// Node.js 환경에서 실행 (ESM 모듈 사용)
import { ethers } from "ethers";

async function getBlockNumber() {
    // Infura 또는 Alchemy와 같은 RPC 제공자 URL 사용
    const provider = new ethers.JsonRpcProvider("https://mainnet.infura.io/v3/YOUR_INFURA_PROJECT_ID");

    // 현재 블록 번호 조회
    const blockNumber = await provider.getBlockNumber();
    console.log("Current block number:", blockNumber);

    // 특정 주소의 잔액 조회
    const balance = await provider.getBalance("0x742d35Cc6634C0532925a3b844Bc454e4438f44e"); // Vitalik Buterin의 주소
    console.log("Vitalik's balance:", ethers.formatEther(balance), "ETH");
}

getBlockNumber();
```

### 2. 스마트 컨트랙트와 상호작용 (읽기 전용 함수 호출)
```javascript
// Node.js 환경에서 실행 (ESM 모듈 사용)
import { ethers } from "ethers";

async function readContract() {
    const provider = new ethers.JsonRpcProvider("https://mainnet.infura.io/v3/YOUR_INFURA_PROJECT_ID");

    // ERC-20 토큰의 ABI (일부만 발췌)
    const abi = [
        "function name() view returns (string)",
        "function symbol() view returns (string)",
        "function totalSupply() view returns (uint256)",
        "function balanceOf(address owner) view returns (uint256)"
    ];

    // USDC 토큰 컨트랙트 주소 (Ethereum Mainnet)
    const usdcAddress = "0xA0b86991c6218b36c1d19D4a2e9Eb0cE3606eB48";

    // Contract 객체 생성
    const usdcContract = new ethers.Contract(usdcAddress, abi, provider);

    // 컨트랙트 함수 호출
    const name = await usdcContract.name();
    const symbol = await usdcContract.symbol();
    const totalSupply = await usdcContract.totalSupply();

    console.log("Token Name:", name);
    console.log("Token Symbol:", symbol);
    console.log("Total Supply:", ethers.formatUnits(totalSupply, 6)); // USDC는 6자리 소수점
}

readContract();
```

### 3. 지갑을 사용하여 트랜잭션 전송 (개인 키 사용)
```javascript
// Node.js 환경에서 실행 (ESM 모듈 사용)
import { ethers } from "ethers";

async function sendTransaction() {
    // 경고: 실제 개인 키를 코드에 직접 노출하는 것은 매우 위험합니다. 환경 변수 등을 사용하세요.
    const privateKey = "YOUR_PRIVATE_KEY"; 
    const recipientAddress = "0xRecipientAddress"; // 수신자 주소
    const amountToSend = "0.001"; // 보낼 이더리움 양 (ETH 단위)

    const provider = new ethers.JsonRpcProvider("https://sepolia.infura.io/v3/YOUR_INFURA_PROJECT_ID"); // 테스트넷 사용 권장
    const wallet = new ethers.Wallet(privateKey, provider);

    console.log("Sending transaction from:", wallet.address);

    const tx = {
        to: recipientAddress,
        value: ethers.parseEther(amountToSend)
    };

    const transactionResponse = await wallet.sendTransaction(tx);
    console.log("Transaction Hash:", transactionResponse.hash);

    // 트랜잭션이 블록에 포함될 때까지 대기
    const receipt = await transactionResponse.wait();
    console.log("Transaction confirmed in block:", receipt.blockNumber);
}

// sendTransaction(); // 실제 트랜잭션을 보내려면 주석을 해제하세요.
```

## 관련 URL
---
[Ethers.js 공식 문서](https://docs.ethers.org/)
[Ethers.js GitHub](https://github.com/ethers-io/ethers.js/)

