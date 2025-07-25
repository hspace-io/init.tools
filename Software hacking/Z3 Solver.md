---
tags:
  - windows
  - mac
  - linux
  - smt_solver
  - math
  - symbolic_execution
  - multi_platform
---
## 설명
---
`Z3 Solver`는 Microsoft Research에서 개발한 SMT(Satisfiability Modulo Theories)솔버 입니다. 논리 공식의 만족 가능성을 확인하고, 복잡한 수학적 제약 조건을 자동으로 해결할 수 있는 정리 증명기입니다. 프로그램 검증, 컴파일러 검증, 테스팅, 퍼징, 모델 기반 소프트웨어 개발, 네트워크 검증, 최적화 등 다양한 솦트웨어 엔지니어링 분야에서 활용됩니다.

## 설치 영역
---
`/path/to/site-package/z3-solver`

## 주요 기능
---
- `SMT 해결`: 논리 공식의 만족 가능성 확인 및 해 찾기
- `다양한 이론 지원`: 산술, 고정 크기 비트 벡터, 확장 배열, 데이터 타입, 해석되지 않은 함수 등
- `수학 방정식 해결`: 선형/비선형 방정식, 부등식 해결
- `논리 표현식 단순화`: 복잡한 논리/수학 표현식을 간결한 형태로 변환
- `제약 만족 문제 해결`: 스도쿠, 스케줄링 등 다양한 문제 해결

## 설치 방법
---
### Python
```sh
pip install z3-solver
```

## 간단 가이드
---
Z3 Solver는 주로 프로그래밍 언어의 라이브러리 형태로 사용됩니다. 여기서는 Python을 이용한 기본적인 사용법을 설명합니다.

1.  **Z3 모듈 임포트**: Python 스크립트 상단에 Z3 모듈을 임포트합니다.
    ```python
    from z3 import *
    ```

2.  **변수 선언**: 정수, 실수, 불리언 등 필요한 변수를 선언합니다.
    ```python
    x = Int('x') # 정수 변수 x
    y = Real('y') # 실수 변수 y
    p = Bool('p') # 불리언 변수 p
    ```

3.  **Solver 객체 생성**: `Solver()`를 호출하여 Solver 객체를 생성합니다.
    ```python
    s = Solver()
    ```

4.  **제약 조건 추가**: `add()` 메서드를 사용하여 제약 조건(수학적/논리적 표현식)을 추가합니다.
    ```python
    s.add(x > 10)
    s.add(x < 20)
    s.add(x % 2 == 0)
    s.add(y == x / 2)
    s.add(Implies(p, x == 12)) # p가 참이면 x는 12
    ```

5.  **만족 가능성 확인**: `check()` 메서드를 호출하여 제약 조건이 만족 가능한지 확인합니다. 결과는 `sat` (만족 가능), `unsat` (만족 불가능), `unknown` 중 하나입니다.
    ```python
    if s.check() == sat:
        print("Solution found:")
        print(s.model()) # 만족하는 모델(변수 값) 출력
    else:
        print("No solution or unknown.")
    ```

#### 예시: 간단한 방정식 풀기
```python
from z3 import *

x = Int('x')
y = Int('y')

s = Solver()
s.add(x + y == 10)
s.add(x - y == 2)

if s.check() == sat:
    m = s.model()
    print(f"x = {m[x]}, y = {m[y]}") # 출력: x = 6, y = 4
else:
    print("No solution.")
```

## 관련 URL
---
[Z3](https://z3prover.github.io/papers/programmingz3.html)
[Z3 GitHub](https://github.com/Z3Prover/z3)
