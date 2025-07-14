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
### Linux
1. 아래의 명령어를 터미널에 입력하여 설치가 가능합니다.
```sh
sudo add-apt-repository ppa:ethereum/ethereum
sudo apt-get update
sudo apt-get install solc
```

### mac
1. 아래의 명령어를 터미널에 입력하여 설치가 가능합니다.
```sh
brew update
brew upgrade
brew tap ethereum/ethereum
brew install solidity
```

### 설치 시 주의 사항
- Windows를 사용하는 경우 Foundryup은 현재 Powershell이나 명령 프롬프트(CMD)를 지원하지 않으므로 GIT BASH 또는 WSL을 설치하여 사용해야 합니다.
- 

## 간단 가이드
---


## 관련 URL
---
[Solidity 웹사이트](https://soliditylang.org/)
[Foundry book](https://book.getfoundry.sh/)
[Foundry Book (Korean Ver.) by 허시원](https://dream-academy.gitbook.io/foundry-book-korean-ver.-by)
