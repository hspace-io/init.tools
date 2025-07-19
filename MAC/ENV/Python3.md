# Python3

## 설명
Python: 간결한 문법과 풍부한 라이브러리를 갖춘 범용 프로그래밍 언어.(인터프리터)

## 설치 영역
`/opt/homebrew/bin`

## 사용처
- 데이터 분석
- 웹 개발
- 머신러닝
- 스크립트 작성

## 설치(접속) 방법
1. **Homebrew를 사용해 Python3 설치:**
   ```bash
   brew install python3
   ```
2. **버전 확인:**
   ```bash
   python --version
   ```

## 설치(접속) 확인
아래 명령어를 실행하여 설치된 Python 버전을 확인:
```bash
python --version
which python
```

출력 예시:
```
Python 3.11.0
/opt/homebrew/bin/python
```

## 주의 사항
- Homebrew로 설치한 Python 버전과 기본 `python --version` 출력값이 다를 수 있습니다.
- macOS에는 기본적으로 Python이 `/usr/bin/python3`에 설치되어 있습니다.
- 아래 명령어를 통해 Homebrew Python을 기본으로 설정하세요:
  ```bash
  open ~/.zshrc
  alias python="/opt/homebrew/bin/python"
  source ~/.zshrc
  python --version
  ```

## 관련 URL
[Python 공식 웹사이트](https://www.python.org)
