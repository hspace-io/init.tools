# Autopsy

## 설명
Autopsy는 디지털 포렌식 분석을 위한 GUI 기반 오픈소스 도구로, 사용자가 디스크 이미지를 분석하고 파일 복구, 타임라인 생성, 이메일 분석 등을 수행할 수 있도록 지원합니다. 이는 법적 디지털 증거 수집 및 조사 목적으로 널리 사용됩니다.

## 설치 영역
Autopsy는 GUI 애플리케이션으로 별도의 설치가 필요합니다.

## 사용처
- 디스크 이미지 분석
- 삭제된 파일 복구
- 웹 브라우저 기록 및 이메일 분석
- 타임라인 생성 및 활동 추적

## 설치(접속) 방법
1. **Autopsy 설치:**
   - [Autopsy 공식 다운로드 페이지](https://www.autopsy.com/download/)에서 설치 파일을 다운로드합니다.
   - macOS에서 Autopsy를 실행하려면 `The Sleuth Kit`을 설치해야 합니다:
     ```bash
     brew install sleuthkit
     ```
   - Autopsy 실행 스크립트를 다운로드한 후 자바 환경에서 실행합니다.

2. **Autopsy 실행:**
   ```bash
   sh autopsy
   ```

## 설치(접속) 확인
Autopsy를 실행하여 새 케이스를 생성하고 디스크 이미지를 불러와 분석 작업이 정상적으로 수행되는지 확인하세요.

## 주의 사항
- Autopsy는 Java 환경이 필요합니다. Java 8 이상이 설치되어 있어야 합니다.
- 파일 시스템 포맷 및 디스크 이미지 지원 여부는 `The Sleuth Kit`에 의존합니다.

## 관련 URL
[Autopsy 공식 웹사이트](https://www.autopsy.com/)
