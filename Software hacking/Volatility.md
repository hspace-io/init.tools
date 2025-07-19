---
tags:
  - windows
  - mac
  - linux
  - forensic
  - memory_analysis
  - multi_platform
---
## 설명
---
`Volatility`는 메모리 덤프 분석을 위한 업계 표준 디지털 포렌식 도구 프레임워크 입니다. 메모리 내의 실행 프로세스, 네트워크 연결, DLL, 레지스트리 키 등 중요한 데이터를 복구 및 분석하는데 사용됩니다.

## 설치 영역
---
`/path/to/site-package/vollatility`

## 주요 기능
---
- 메모리 덤프 분석
- 악성코드 탐지 및 제거
- 디지털 포렌식 사고 대응

## 설치 방법
---
### Python
- 아래의 명령어들을 터미널에 입력하여 설치 할 수 있습니다.
```sh
git clone https://github.com/volatilityfoundation/volatility3.git
cd vollatility3
python3 setup.py install
```

## 간단 가이드
---
- 실행 방법
- Volatility를 실행한 후 사용 가능한 플러그인 목록을 확인하려면 아래의 명령어를 실행하시면 됩니다.
```sh
python3 vol.py -h
```

## 관련 URL
---
[Volatility 공식 GitHub 저장소](https://github.com/volatilityfoundation/volatility3)
