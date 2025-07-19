# GEF

## 설명
GDB의 대표적인 플러그인중 하나

## 사용처

- 동적 디버깅

## 설치 방법

1. **GEF 설치:**
   ```bash
   wget -O ~/.gdbinit-gef.py https://gef.blah.cat/py
   echo "source ~/.gdbinit-gef.py" >> ~/.gdbinit
   ```
2. **설치 확인:**
   ```bash
   gdb
   ```
   GDB 실행 후, GEF 로고가 표시되면 정상 설치됨.

## 관련 URL

[GEF 공식 문서](https://github.com/hugsy/gef)
