# Frida

## 설명
- Windows, macOS, Linux, iOS, Android, and QNX 기반의 네이티앱에 대해 후킹
- c로 개발되어있지만 python을 이용하여 구현된 모듈이 존재합니다.


### python 환경

> pip install frida

- frida 만 설치하고 싶으신 분은 위 명령어를 사용하면 됩니다. 

> pip install frida-tools
- frida 뿐만 아니

### Frida 설치 영역
- window wsl

## 사용처
- 바이너리 후킹
- DBI (Dynamic Binary Instrumentation) 바이너리 실행시 동작 분석

```python
# test.py
import frida

def on_message(message, data):
    print("[on_message] message:", message, "data:", data)

session = frida.attach("cat")

script = session.create_script("""
rpc.exports.enumerateModules = () => {
  return Process.enumerateModules();
};
""")
script.on("message", on_message)
script.load()

print([m["name"] for m in script.exports_sync.enumerate_modules()])
```

- 위 코드는 `cat` 명령어를 후킹하는 예시 코드입니다.
- `test.py`로 저장한 후, 다른 커맨드라인에서 `cat` 명령어를 실행합니다.

```bash
$python example.py
['cat', 'linux-vdso.so.1', 'libc.so.6', 'ld-linux-x86-64.so.2', ...  ,'libpthread.so.0']
```

- 파이썬 코드 실행 시 `cat` 프로세스와 관련된 라이브러리, 링커 등 다양한 파일들을 출력하게 됩니다.

### Frida server 설치
- 후킹 대상에 서버를 설치
- 분석 대상 기기에도 firda-server 를 설치해야 합니다.

[Frida](https://github.com/frida/frida/releases)

- 설치하려는 버전으로 들어가면, 후킹 대상 아키텍쳐에 맞는 frida-server를 선택합니다.

[Frida](https://github.com/frida/frida/releases/tag/16.6.6)

## 관련 URL
[Frida Github](https://github.com/frida/frida/releases)
[Frida Docs](https://frida.re)