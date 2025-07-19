# C Language

## 설명
C언어는 시스템 프로그래밍 및 저수준 작업에 최적화된 프로그래밍 언어입니다. 컴파일러를 통해 실행 파일로 변환되어 효율적이고 빠른 실행 속도를 제공합니다.

## 설치 영역
`/Library/Developer/CommandLineTools/usr/bin`

## 사용처
- 임베디드 시스템 개발
- 운영체제 개발
- 성능이 중요한 애플리케이션 개발
- 하드웨어 제어 및 시스템 프로그래밍

## 설치(접속) 방법
1. **기본 설치**
   - macOS에는 기본적으로 C언어 컴파일러(Command Line Tools)가 설치되어 있습니다.
   - 명령어로 설치 상태를 확인할 수 있습니다:
     ```bash
     gcc --version
     g++ --version
     clang --version
     ```

2. **설치가 필요할 경우**
   - Homebrew를 사용하여 추가적인 컴파일러를 설치할 수 있습니다:
     ```bash
     brew install gcc
     ```

## 설치(접속) 확인
다음 명령어를 실행하여 설치된 컴파일러의 버전을 확인할 수 있습니다:
```bash
gcc --version
g++ --version
clang --version
```

예시 출력:
```
Apple clang version 16.0.0 (clang-1600.0.26.4)
Target: arm64-apple-darwin21.1.0
Thread model: posix
InstalledDir: /Library/Developer/CommandLineTools/usr/bin
```

## 주의 사항
- macOS에서는 Command Line Tools가 설치되어 있어야 `gcc`, `g++`, 및 `clang` 명령어를 사용할 수 있습니다.
- 프로젝트에 필요한 특정 C 컴파일러 버전이 있는 경우, 추가 설치가 필요할 수 있습니다.

## 관련 URL
- [C 언어 학습 리소스](https://www.learn-c.org/)
