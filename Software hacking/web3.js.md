## 설명
---
`Web3.js`는 이더리움 블록체인과 상호작용하기 위한 JavaScript 라이브러리입니다. 웹 애플리케이션(프론트엔드) 및 Node.js 환경(백엔드)에서 이더리움 노드와 통신하고, 스마트 컨트랙트를 배포 및 호출하며, 트랜잭션을 관리하는 등 다양한 블록체인 관련 작업을 수행할 수 있도록 설계되었습니다.

## 설치 영역
---
`Web3.js`는 JavaScript 라이브러리이므로, 프로젝트의 `node_modules` 디렉토리에 설치됩니다. 특정 고정된 시스템 경로는 없습니다.

## 주요 기능
---
- `이더리움 노드 연결`: HTTP, IPC, WebSocket을 통해 이더리움 노드에 연결
- `계정 관리`: 이더리움 계정 생성, 가져오기, 서명, 트랜잭션 전송
- `스마트 컨트랙트 상호작용`: 컨트랙트의 ABI(Application Binary Interface)를 사용하여 컨트랙트 함수 호출 및 이벤트 수신
- `트랜잭션 관리`: 트랜잭션 생성, 서명, 전송 및 상태 추적
- `유틸리티 함수`: 이더리움 주소 유효성 검사, 단위 변환(wei, ether), 해시 함수 등 다양한 유틸리티 제공
- `이벤트 리스너`: 블록체인 이벤트(새로운 블록, 컨트랙트 이벤트 등)를 실시간으로 수신

## 설치 방법
---
`Web3.js`는 npm(Node Package Manager)을 통해 프로젝트에 설치합니다.

1.  **Node.js 및 npm 설치**: 시스템에 Node.js와 npm이 설치되어 있어야 합니다.
2.  **프로젝트 초기화 (선택 사항)**: 새 프로젝트에서 시작하는 경우 `npm init -y` 명령어로 `package.json` 파일을 생성합니다.
3.  **Web3.js 설치**: 프로젝트 디렉토리에서 다음 명령어를 실행합니다.
    ```sh
    npm install web3
    ```
    또는 `yarn`을 사용하는 경우:
    ```sh
    yarn add web3
    ```

## 간단 가이드
---
### 1. 이더리움 노드 연결
```javascript
// Node.js 환경에서 실행
const Web3 = require('web3');

// Infura 또는 Alchemy와 같은 RPC 제공자 URL 사용
const web3 = new Web3('https://mainnet.infura.io/v3/YOUR_INFURA_PROJECT_ID');

async function getBlockNumber() {
    const blockNumber = await web3.eth.getBlockNumber();
    console.log('Current block number:', blockNumber);

    const balance = await web3.eth.getBalance('0x742d35Cc6634C0532925a3b844Bc454e4438f44e'); // Vitalik Buterin의 주소
    console.log('Vitalik\'s balance:', web3.utils.fromWei(balance, 'ether'), 'ETH');
}

getBlockNumber();
```

### 2. 스마트 컨트랙트와 상호작용 (읽기 전용 함수 호출)
```javascript
// Node.js 환경에서 실행
const Web3 = require('web3');
const web3 = new Web3('https://mainnet.infura.io/v3/YOUR_INFURA_PROJECT_ID');

async function readContract() {
    // ERC-20 토큰의 ABI (일부만 발췌)
    const abi = [
        { "constant": true, "inputs": [], "name": "name", "outputs": [{ "name": "", "type": "string" }], "payable": false, "stateMutability": "view", "type": "function" },
        { "constant": true, "inputs": [], "name": "symbol", "outputs": [{ "name": "", "type": "string" }], "payable": false, "stateMutability": "view", "type": "function" },
        { "constant": true, "inputs": [], "name": "totalSupply", "outputs": [{ "name": "", "type": "uint256" }], "payable": false, "stateMutability": "view", "type": "function" },
        { "constant": true, "inputs": [{ "name": "_owner", "type": "address" }], "name": "balanceOf", "outputs": [{ "name": "balance", "type": "uint256" }], "payable": false, "stateMutability": "view", "type": "function" }
    ];

    // USDC 토큰 컨트랙트 주소 (Ethereum Mainnet)
    const usdcAddress = '0xA0b86991c6218b36c1d19D4a2e9Eb0cE3606eB48';

    // Contract 객체 생성
    const usdcContract = new web3.eth.Contract(abi, usdcAddress);

    // 컨트랙트 함수 호출
    const name = await usdcContract.methods.name().call();
    const symbol = await usdcContract.methods.symbol().call();
    const totalSupply = await usdcContract.methods.totalSupply().call();

    console.log('Token Name:', name);
    console.log('Token Symbol:', symbol);
    console.log('Total Supply:', web3.utils.fromWei(totalSupply, 'mwei')); // USDC는 6자리 소수점
}

readContract();
```

### 3. 트랜잭션 전송 (개인 키 사용)
```javascript
// Node.js 환경에서 실행
const Web3 = require('web3');
const web3 = new Web3('https://sepolia.infura.io/v3/YOUR_INFURA_PROJECT_ID'); // 테스트넷 사용 권장

async function sendTransaction() {
    // 경고: 실제 개인 키를 코드에 직접 노출하는 것은 매우 위험합니다. 환경 변수 등을 사용하세요.
    const privateKey = 'YOUR_PRIVATE_KEY'; 
    const senderAddress = web3.eth.accounts.privateKeyToAccount(privateKey).address;
    const recipientAddress = '0xRecipientAddress'; // 수신자 주소
    const amountToSend = web3.utils.toWei('0.001', 'ether'); // 보낼 이더리움 양 (wei 단위)

    const transaction = {
        from: senderAddress,
        to: recipientAddress,
        value: amountToSend,
        gas: 21000, // 일반적인 이더 전송 가스 한도
        // gasPrice: await web3.eth.getGasPrice() // 현재 가스 가격
    };

    const signedTx = await web3.eth.accounts.signTransaction(transaction, privateKey);
    const receipt = await web3.eth.sendSignedTransaction(signedTx.rawTransaction);

    console.log('Transaction Hash:', receipt.transactionHash);
    console.log('Transaction confirmed in block:', receipt.blockNumber);
}

// sendTransaction(); // 실제 트랜잭션을 보내려면 주석을 해제하세요.
```

## 관련 URL
---
[Web3.js 공식 문서](https://web3js.readthedocs.io/en/v1.x/)
[Web3.js GitHub](https://github.com/web3/web3.js)
