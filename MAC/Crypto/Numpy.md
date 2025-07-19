# Numpy

## 설명
NumPy는 Python에서 고성능 수치 연산과 다차원 배열 처리를 지원하는 라이브러리입니다. 
주로 과학 연산, 데이터 분석, 머신러닝 등의 분야에서 사용됩니다.

## 설치 영역
- Python 패키지 경로: `/path/to/site-packages/numpy`

## 사용처
- 벡터 및 행렬 연산
- 통계 및 수치 해석
- 과학적 데이터 처리 및 시뮬레이션

## 설치(접속) 방법
1. **pip를 사용하여 설치:**
   ```bash
   pip install numpy
   ```
2. **설치 확인:**
   ```bash
   python -c "import numpy; print(numpy.__version__)"
   ```
   ```bash
   pip show numpy
   ```

## 접속 화면
```
>>> pip show numpy
Name: numpy
Version: 1.26.4
Summary: Fundamental package for array computing in Python
Home-page: https://numpy.org
Author: Travis E. Oliphant et al.
Author-email:
License: Copyright (c) 2005-2023, NumPy Developers.
All rights reserved.
...
```

## 주의 사항
- NumPy는 최신 Python 버전과 호환되도록 주기적으로 업데이트됩니다.
- 고성능 연산을 위해 C 및 Fortran 기반 라이브러리를 활용하므로, 일부 시스템에서는 컴파일러 설정이 필요할 수 있습니다.

## 관련 URL
- [NumPy 공식 웹사이트](https://numpy.org/)
- [NumPy 공식 문서](https://numpy.org/doc/)
