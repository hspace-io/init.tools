# PyCryptodome

## 설명
PyCryptodome은 Python에서 암호화 작업을 수행할 수 있도록 지원하는 라이브러리로, 다양한 암호화 알고리즘과 도구를 제공합니다. AES, RSA, SHA-256 등 현대적인 암호화 방식을 구현할 수 있습니다.

## 설치 영역
- Python 패키지 경로: `/path/to/site-packages/Cryptodome`

## 사용처
- 대칭 및 비대칭 키 암호화
- 디지털 서명 및 인증
- 해시 및 데이터 무결성 검사

## 설치(접속) 방법
1. **pip를 사용하여 설치:**
   ```bash
   pip install pycryptodome
   ```
2. **설치 확인:**
   ```bash
   python -c "from Cryptodome.Cipher import AES; print('PyCryptodome 설치 성공')"
   ```

## 정상 체크 화면
```plaintext
>>> python -c "from Cryptodome.Cipher import AES; print('PyCryptodome 설치 성공')"
PyCryptodome 설치 성공
```

## 주의 사항
- PyCryptodome은 Python 3.6 이상에서만 작동합니다.
- 보안 목적으로 강력한 암호화 키와 알고리즘을 선택해야 합니다.

## 관련 URL
- [PyCryptodome GitHub 페이지](https://github.com/Legrandin/pycryptodome)
- [PyCryptodome 공식 문서](https://pycryptodome.readthedocs.io/)
