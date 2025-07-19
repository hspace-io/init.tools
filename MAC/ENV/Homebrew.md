# Homebrew

## 설명
Homebrew는 macOS 및 Linux에서 소프트웨어를 설치하고 관리하기 위한 패키지 관리자입니다. 터미널 명령어를 통해 간단하고 효율적으로 다양한 오픈소스 소프트웨어를 설치, 업데이트, 삭제할 수 있습니다.

## 설치 영역
Homebrew는 기본적으로 다음 경로에 설치됩니다:
- Intel Mac: `/usr/local`
- Apple Silicon (M1/M2): `/opt/homebrew`

## 사용처
- macOS 및 Linux 환경에서 필수 도구 설치 및 관리
- 개발 환경 설정 자동화
- 의존성 있는 소프트웨어 설치 및 업데이트
- 서버 및 로컬 개발환경 유지보수

## 설치(접속) 방법
1. **Homebrew 설치**
   터미널에서 다음 명령어를 실행하세요:
   ```bash
   /bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
   ```

2. **설치 확인**
   설치가 완료되었는지 아래 명령어로 확인하세요:
   ```bash
   brew --version
   ```

3. **Homebrew 사용 예시**
   - 소프트웨어 설치:
     ```bash
     brew install [패키지명]
     ```
   - 패키지 목록 확인:
     ```bash
     brew list
     ```
   - 업데이트 및 업그레이드:
     ```bash
     brew update
     brew upgrade
     ```

## 접속 화면
Homebrew는 CLI 기반 도구이며, GUI를 제공하지 않습니다. 아래는 `brew --version` 명령어 실행 화면의 예입니다:

```
Homebrew 4.x.x
Homebrew/homebrew-core (git revision abc123; last commit 2025-01-01)
```

## 주의 사항
- 인터넷 연결이 필요하며, 설치 시 네트워크 속도에 따라 시간이 걸릴 수 있습니다.
- 설치 경로는 시스템 구조(Intel vs Apple Silicon)에 따라 다릅니다:
  - Intel Mac: `/usr/local`
  - Apple Silicon: `/opt/homebrew`
- 아래 명령어로 Homebrew 및 설치된 패키지를 정기적으로 업데이트하는 것이 좋습니다:
  ```bash
  brew update
  brew upgrade
  ```

## 관련 URL
- [Homebrew 공식 웹사이트](https://brew.sh)
- [Homebrew GitHub 저장소](https://github.com/Homebrew/brew)
