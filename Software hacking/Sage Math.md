---
tags:
  - windows
  - mac
  - linux
  - math
  - crypto
  - science_tool
---
## 설명
---
`SageMath`는 수학 및 암호학 연산을 수행하기 위한 오픈소스 소프트웨어로, 다양한 수학적 기능과 대수학, 통계학, 그래프 이론 등을 지원합니다.

## 설치 영역
---
### Windows
`C:\Program Files\SageMath {version}` (설치 시 지정)

### mac
`/Applications/SageMath-{version}.app` (설치 시 지정)

### Linux
`/usr/bin/sage` (패키지 설치 시)

## 주요 기능
---
- `수학적 모델링 및 해석`
- `암호학 연구 및 프로토타입 개발`
- `과학적 계산과 데이터 시각화`

## 설치 방법
---
### Conda
- Conda를 이용하는 경우 가상환경을 만들고 진행하는 것을 추천드립니다.
- 아래의 명령어를 터미널에 입력하시면 설치가 가능합니다.
```sh
conda install -c conda-forge sage
```

### Linux
```sh
sudo apt install sagemath
```

### mac
1.  [SageMath 공식 웹사이트](https://www.sagemath.org/download.html)에서 macOS용 설치 파일(.dmg)을 다운로드합니다.
2.  다운로드한 `.dmg` 파일을 열고, `SageMath-{version}.app`을 `Applications` 폴더로 드래그하여 설치합니다.

## 간단 가이드
---
1.  **SageMath 실행**: 터미널에서 `sage`를 입력하여 SageMath 쉘을 실행합니다.
    ```sh
    sage
    ```
    *   GUI 환경을 사용하려면 `sage -n jupyter` 명령어로 Jupyter Notebook을 실행할 수 있습니다.

2.  **기본 연산**: 일반적인 수학 연산을 수행합니다.
    ```python
    2 + 2
    factor(12345)
    solve(x^2 - 1 == 0, x)
    ```

3.  **변수 정의 및 함수 사용**: 변수를 정의하고 함수를 사용하여 복잡한 계산을 수행합니다.
    ```python
    var('x, y')
    f(x) = x^2 + 3*x + 2
    f(5)
    diff(f(x), x) # 미분
    integrate(f(x), x) # 적분
    ```

4.  **암호학 관련 기능**: 소수 판별, 유클리드 호제법, 모듈러 연산 등 암호학에 필요한 기능을 사용합니다.
    ```python
    is_prime(97)
    gcd(123, 456)
    power_mod(7, 100, 13) # 7^100 mod 13
    ```

5.  **그래프 그리기**: 2D 및 3D 그래프를 그릴 수 있습니다.
    ```python
    plot(sin(x), (x, 0, 2*pi))
    plot3d(x^2 + y^2, (x, -2, 2), (y, -2, 2))
    ```

- 설치 이후 터미널에 `sage`를 입력하시면 SageMath를 이용할 수 있습니다.

## 관련 URL
---
[SageMath 공식 웹사이트](https://www.sagemath.org/)
[SageMath 공식 문서](https://doc.sagemath.org/)
[SageMath 튜토리얼](https://blog.hspace.io/posts/SageMath-tutorial-1/)
