---
tags:
  - windows
  - mac
  - linux
  - pwnable
  - python
  - library
  - exploit_framework
  - multi_platform
---
## 설명
---
CTF (Wargame) 프레임워크이자 익스플로잇 개발을 위한 파이썬 라이브러리

## 설치 영역
---
`/path/to/site-packages/pwntools`

## 주요 기능
---
- 네트워크 통신 및 프로세스 상호작용
- 데이터 패킹/언패킹
- ELF 바이너리 분석
- ROP 체인 구성
- 쉘코드 생성 및 디스어셈블리
- 입출력 기능

## 설치 방법
---
- 아래 명령어를 터미널에 입력하여 설치 가능합니다.
```sh
pip install pwntools
```

## 간단 가이드
---
`pwntools`는 Python 라이브러리이므로, Python 스크립트 내에서 사용됩니다.

1.  **원격 서비스 연결 및 상호작용**:
    ```python
    from pwn import *

    # 원격 호스트와 포트에 연결
    r = remote("example.com", 1234)

    # 데이터 수신
    data = r.recvline()
    print(f"Received: {data.decode()}")

    # 데이터 전송
    r.sendline(b"Hello, server!")

    # 특정 문자열까지 수신
    r.recvuntil(b"Prompt: ")

    # 쉘 획득 (대화형 모드)
    r.interactive()

    # 연결 종료
    r.close()
    ```

2.  **로컬 프로세스 실행 및 상호작용**:
    ```python
    from pwn import *

    # 로컬 실행 파일 실행
    p = process("./a.out")

    # 데이터 수신 및 전송은 remote와 동일
    p.recvuntil(b"Input: ")
    p.sendline(b"A" * 100)

    # 쉘 획득
    p.interactive()

    p.close()
    ```

3.  **값 패킹/언패킹**: 익스플로잇 개발 시 주소나 정수 값을 바이트 형태로 변환하거나 그 반대로 변환할 때 사용합니다.
    ```python
    from pwn import *

    # 32비트 정수 패킹 (little-endian)
    packed_val = p32(0xdeadbeef)
    print(f"Packed: {packed_val}") # b'\xef\xbe\xad\xde'

    # 64비트 정수 패킹 (little-endian)
    packed_long = p64(0x1122334455667788)
    print(f"Packed long: {packed_long}") # b'\x88wVUPTSR\x11'

    # 언패킹
    unpacked_val = u32(b'\xef\xbe\xad\xde')
    print(f"Unpacked: {hex(unpacked_val)}") # 0xdeadbeef
    ```

4.  **ELF 바이너리 분석**: ELF 파일의 섹션, 심볼, 주소 등을 분석합니다.
    ```python
    from pwn import *

    elf = ELF("./a.out")

    print(f"Entry point: {hex(elf.entry)}")
    print(f"Address of main: {hex(elf.symbols.main)}")
    print(f"Address of puts@got: {hex(elf.got.puts)}")
    ```

## 관련 URL
---
[pwntools GitHub 페이지](https://github.com/Gallopsled/pwntools)
[pwntools 공식 문서](http://docs.pwntools.com/en/stable/#)
