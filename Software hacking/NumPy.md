---
tags:
  - windows
  - mac
  - linux
  - math
  - science_tool
  - library
  - multi_platform
  - python
---
## 설명
---
`NumPy`는 Python에서 고성능 수치 연산과 다차원 배열 처리를 지원하는 라이브러리입니다. 주로 과학 연산, 데이터 분석, 머신러닝 등의 분야에서 사용됩니다.

## 설치 영역
---
### Windows
- Python 패키지 경로: `/path/to/site-packages/numpy`

### Linux
- Python 패키지 경로: `/path/to/site-packages/numpy`

### mac
- Python 패키지 경로: `/path/to/site-packages/numpy`

## 주요 기능
---
- `N차원 배열 객체`: 고성능 다차원 배열 자료구조 제공
- `벡터/행렬 연산`: 벡터화 연산, 브로드캐스팅, 선형대수, 통계 등 지원
- `고속 수치 연산`: C로 구현된 내부 구조로 매우 빠른 연산 속도 제공
- `난수 생성`
- `파일 입출력`: 바이너리(.npy, .npz) 및 텍스트 파일 입출력 지원
- `선형대수, 푸리에 변환, 통계, 집계 등 과학 계산 함수 다수 내장`
- `다양한 외부 라이브러리와 연동`: pnada, matplotlib, scikit-learn 등과 호환성 우수

## 설치 방법
---
- 아래의 명령어를 터미널에 입력하여 설치하시면 됩니다.
```sh
pip install numpy
```

설치 시 주의 사항
- NumPy 설치를 위해서는 Python과 pip가 설치되어 있어야 합니다.

## 간단 가이드
---
1.  **NumPy 임포트**: Python 스크립트나 인터프리터에서 NumPy를 사용하려면 먼저 임포트해야 합니다.
    ```python
    import numpy as np
    ```

2.  **배열 생성**: `np.array()` 함수를 사용하여 NumPy 배열(ndarray)을 생성합니다.
    ```python
    # 1차원 배열
    arr1 = np.array([1, 2, 3, 4, 5])
    print(arr1)

    # 2차원 배열 (행렬)
    arr2 = np.array([[1, 2, 3], [4, 5, 6]])
    print(arr2)

    # 0으로 채워진 배열
    zeros = np.zeros((2, 3))
    print(zeros)

    # 1로 채워진 배열
    ones = np.ones((3, 2))
    print(ones)

    # 특정 범위의 숫자 배열
    arange = np.arange(0, 10, 2) # 0부터 10 미만까지 2씩 증가
    print(arange)
    ```

3.  **배열 연산**: NumPy 배열은 일반 Python 리스트와 달리 벡터화된 연산을 지원하여 빠르고 효율적입니다.
    ```python
    arr_a = np.array([1, 2, 3])
    arr_b = np.array([4, 5, 6])

    # 요소별 덧셈
    print(arr_a + arr_b)

    # 요소별 곱셈
    print(arr_a * 2)

    # 행렬 곱셈 (dot product)
    matrix_a = np.array([[1, 2], [3, 4]])
    matrix_b = np.array([[5, 6], [7, 8]])
    print(np.dot(matrix_a, matrix_b))
    ```

4.  **배열 인덱싱 및 슬라이싱**: Python 리스트와 유사하게 인덱싱과 슬라이싱을 사용할 수 있습니다.
    ```python
    arr = np.array([[1, 2, 3], [4, 5, 6], [7, 8, 9]])

    # 특정 요소 접근
    print(arr[0, 0]) # 1

    # 행 슬라이싱
    print(arr[0:2, :]) # 첫 두 행

    # 열 슬라이싱
    print(arr[:, 1]) # 두 번째 열
    ```

5.  **통계 함수**: 평균, 합계, 표준편차 등 다양한 통계 함수를 제공합니다.
    ```python
    data = np.array([10, 20, 30, 40, 50])
    print(np.mean(data)) # 평균
    print(np.sum(data))  # 합계
    print(np.std(data))  # 표준편차
    ```
