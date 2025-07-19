---
tags:
  - web_base_tool
  - crypto
  - data_processing
---
## 설명
---
`CyberChef`는 다양한 데이터 분석 및 변환 작업을 지원하는 웹 기반 도구입니다. 암호화, 인코딩/디코딩, 데이터 변환 등 여러 기능을 하나의 인터페이스에서 사용 할 수 있습니다. "데이터 요리사"로 불리며, 직관적인 UI 를 제공하여 복잡한 작업을 간단히 수행할 수 있습니다.

## 설치 영역
---
`웹 기반 도구 - 별도 설치 필요 없음`
오프라인 작업을 위해서 다운로드 받아서 사용 가능

## 주요 기능
---
- 암호화 및 디코딩 작업
- 데이터 변환 (Base64, Hex, URL Encoding/Decoding 등)
- 해시 생성 (MD5, SHA-256 등)
- 파일 분석 및 문자열 추출
- 다양한 데이터 포맷 간 변환

## 설치/접속 방법
---
#### Online
`CyberChef` [공식 웹 사이트에](https://cyberchef.io/) 접속해서 원하는 작업을 진행하시면 됩니다.

#### Offline
1. `CyberChef` 깃허브나, [공식 웹 사이트에](https://cyberchef.io/)의 좌상단에 있는 `Download CyberChef` 버튼을 눌러 압축 파일을 다운 받습니다. 
2. 다운 받은 파일의 압축을 해제한 뒤 `CyberChef_{version}.html`을 브라우저를 통해서 열면 사용이 가능합니다.

## 간단 가이드
---
1.  **입력 (Input)**: 오른쪽 상단의 `Input` 창에 분석하거나 변환할 데이터를 붙여넣습니다.

2.  **기능 선택 (Operations)**: 왼쪽의 `Operations` 목록에서 원하는 기능을 검색하거나 찾아서 선택합니다. 예를 들어, `From Base64`를 검색하여 선택합니다.

3.  **레시피 구성 (Recipe)**: 선택한 기능은 가운데 `Recipe` 창으로 드래그 앤 드롭하여 추가합니다. 여러 기능을 순차적으로 연결하여 복잡한 변환 파이프라인을 만들 수 있습니다.
    *   예시: `From Base64` -> `Gunzip` -> `To Hex`

4.  **출력 확인 (Output)**: `Recipe`가 적용된 결과는 오른쪽 하단의 `Output` 창에 실시간으로 표시됩니다.

5.  **레시피 저장 및 공유**: `Save Recipe` 버튼을 눌러 현재 구성한 레시피를 저장하거나, URL을 통해 다른 사람과 공유할 수 있습니다.

#### 예시: Base64로 인코딩된 압축 데이터를 16진수로 변환하기
1.  `Input` 창에 Base64 문자열을 입력합니다.
2.  `Operations`에서 `From Base64`를 찾아 `Recipe`로 드래그합니다.
3.  `Operations`에서 `Gunzip`을 찾아 `From Base64` 아래에 추가합니다.
4.  `Operations`에서 `To Hex`를 찾아 `Gunzip` 아래에 추가합니다.
5.  `Output` 창에서 최종 16진수 변환 결과를 확인합니다.


## 관련 URL
---
[공식 웹 사이트에](https://cyberchef.io/)
