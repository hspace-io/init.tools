# Volatility

## 설명
Volatility는 메모리 덤프 분석을 위한 업계 표준 디지털 포렌식 프레임워크입니다. 메모리 내의 실행 프로세스, 네트워크 연결, DLL, 레지스트리 키 등 중요한 데이터를 복구 및 분석하는 데 사용됩니다.

## 설치 영역
Volatility는 설치형 애플리케이션이 아닌 Python 기반 CLI 도구로 제공됩니다.

## 사용처
- 메모리 덤프 분석
- 악성코드 탐지 및 제거
- 디지털 포렌식 및 사고 대응

## 설치(접속) 방법
1. **Volatility 설치:**
   - 최신 Volatility 3 버전을 GitHub에서 다운로드:
     ```bash
     git clone https://github.com/volatilityfoundation/volatility3.git
     cd volatility3
     python3 setup.py install
     ```

2. **Volatility 실행:**
   ```bash
   python3 vol.py -h
   ```

## 설치(접속) 확인
Volatility를 실행한 후 사용 가능한 플러그인 목록을 확인하려면 아래 명령어를 실행하세요:
```bash
python3 vol.py -h
```

출력 예시:
```
Volatility Framework 3.0
Usage: vol.py [options]
```

## 주의 사항
- Python3 및 관련 패키지가 필요합니다. Homebrew로 Python3을 설치하거나, 가상 환경(virtualenv)을 설정하는 것이 권장됩니다.
- 분석할 메모리 덤프는 `.raw`, `.mem`, `.lime` 등의 포맷을 지원합니다.

## 관련 URL
[Volatility 공식 GitHub 저장소](https://github.com/volatilityfoundation/volatility3)
