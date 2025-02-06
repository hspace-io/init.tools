# pwndbg
## 설명
포너블(Pwnable)에 특화된 GDB(GNU Debugger) 플러그인. \
기존 GDB에 비하여 많은 편리한 기능을 제공하기 때문에 리눅스에서 범용적으로 사용하기에도 좋다. 

## 설치 영역
GDB 플러그인은 기본적으로 `~/.gdbinit` 파일을 읽어와서 로딩된다. 설치시 자동으로 해당 파일에 pwndbg 를 다운받은 경로를 추가한다. 따라서 설치 영역은 사용자가 pwndbg 를 다운받은 경로이다. 

## 사용처
- 리눅스 환경에서 동적디버깅

## 설치(접속) 방법
```bash
git clone https://github.com/pwndbg/pwndbg
cd pwndbg
./setup.sh
```
이후 gdb 실행시 자동으로 pwndbg가 적용된다. 

## 주로 사용하는 명령어어
`vmmap` : 프로세스의 메모리 맵 출력 \
`tele` : 해당 주소를 자세히 조사. 주소가 포인터라면 포인터를 계속 따라가며 출력 \
`search` : 특정 문자열이나 바이트 배열을 검색 \
`heap, bins` : 힙 관련 구조체들을 정리해서 보여줌 (ptmalloc2)

## 관련 URL
[pwndbg 깃허브](https://github.com/pwndbg/pwndbg) \
[기능 모음](https://github.com/pwndbg/pwndbg/blob/dev/FEATURES.md) \
[한눈에 보는 명령어 모음](https://drive.google.com/file/d/16t9MV8KTFXK7oX_CzXhmDdaVnjT8IYM4/view)