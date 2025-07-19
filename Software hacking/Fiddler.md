---
tags:
  - mac
  - windows
  - linux
  - debugging
  - web
  - network
  - application
  - http_proxy
---
## 설명
---
`Fiddler`는 HTTP 및 HTTPS 트래픽 디버깅 도구로, 요청 및 응답을 가로채고 수정할 수 있습니다.

## 설치 영역
---
### Windows
`C:\Program Files (x86)\Fiddler2` (기본 설치 경로, 사용자 설정에 따라 달라질 수 있음)

### mac
`/Applications/Fiddler.app`

## 주요 기능
---
- HTTP 및 HTTPS 트래픽 디버깅
- API 요청 및 응답 분석
- 네트워크 오류 추적

## 설치 방법
---
1. Fiddler 다운로드: [공식 웹사이트]([https://www.telerik.com/fiddler/fiddler-classic](https://www.telerik.com/fiddler/fiddler-classic))에서 Fiddler Classic 설치 파일을 다운로드합니다.
2. 설치 파일 실행: 다운로드한 설치 파일을 실행하고, 안내에 따라 설치를 진행합니다. 기본 설정을 사용해도 무방합니다.
3. Fiddler 실행: 설치가 완료되면 Fiddler를 실행합니다. 처음 실행 시 HTTPS 트래픽 캡처를 위한 인증서 설치 여부를 묻는 창이 나타날 수 있습니다. HTTPS 트래픽을 캡처하려면 인증서를 설치해야 합니다. (보안에 주의하여 설치 여부를 결정하세요.)
4. 트래픽 캡처 시작: Fiddler는 자동으로 시스템 프록시로 설정되어 실행 즉시 HTTP 트래픽을 캡처하기 시작합니다. 왼쪽 하단의 "Capturing" 표시를 확인하세요. 캡처를 중지하려면 이 부분을 클릭하거나, File > Capture Traffic (F12) 메뉴를 사용합니다.

## 간단 가이드
---
1.  **트래픽 캡처**: Fiddler를 실행하면 기본적으로 트래픽 캡처가 시작됩니다. 왼쪽 `Web Sessions` 목록에 HTTP/HTTPS 요청이 실시간으로 표시됩니다. 캡처를 중지하거나 다시 시작하려면 `File > Capture Traffic` (F12)를 토글합니다.

2.  **HTTPS 트래픽 복호화**: HTTPS 트래픽을 보려면 `Tools > Options > HTTPS` 탭으로 이동하여 `Decrypt HTTPS traffic`을 체크해야 합니다. 이 과정에서 Fiddler의 루트 인증서를 신뢰하도록 설치해야 합니다.

3.  **요청/응답 분석**: `Web Sessions` 목록에서 특정 세션을 클릭하면, 오른쪽 패널에서 상세 정보를 볼 수 있습니다.
    *   `Inspectors` 탭: 요청과 응답의 내용을 다양한 뷰(헤더, 텍스트, JSON, 헥스 등)로 분석할 수 있습니다.
    *   `Timeline` 탭: 각 요청의 성능(소요 시간)을 시각적으로 보여줍니다.

4.  **요청 수정 및 재전송 (Composer)**:
    *   `Composer` 탭으로 이동하여 직접 HTTP 요청을 만들거나, `Web Sessions` 목록의 요청을 드래그하여 가져올 수 있습니다.
    *   메서드, URL, 헤더, 본문 등을 수정한 후 `Execute` 버튼을 눌러 서버로 요청을 보낼 수 있습니다.

5.  **자동 응답 (AutoResponder)**:
    *   `AutoResponder` 탭으로 이동하여 특정 조건에 맞는 요청이 들어왔을 때, 미리 정의된 로컬 파일이나 다른 응답으로 자동으로 응답하도록 설정할 수 있습니다. 웹 개발 및 테스트 시 유용합니다.

### 사용 시 주의 사항
- Fiddler는 일부 고급 기능이 유료로 제공됩니다.
- HTTPS 트래픽 디버깅 SSL 인증서 설정이 피룡할 수 있습니다.

## 관련 URL
---
[Fiddler Classic 공식 웹사이트](https://www.telerik.com/fiddler/fiddler-classic)
[Fiddler 설명서](https://docs.telerik.com/fiddler/fiddler-classic)
[Fiddler Everywhere (크로스 플랫폼 버전)](https://www.telerik.com/fiddler)
