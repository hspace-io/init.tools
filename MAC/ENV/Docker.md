# Docker

## 설명
Docker는 컨테이너화된 애플리케이션을 구축, 배포 및 실행하는 오픈소스 플랫폼입니다. 경량화된 컨테이너 기술을 통해 개발 및 운영 환경의 일관성을 유지할 수 있습니다.

## 설치 영역
`/Applications/Docker.app`

## 사용처
- 애플리케이션 컨테이너화
- 개발 및 테스트 환경의 표준화
- 마이크로서비스 아키텍처 구현
- 배포 자동화

## 설치(접속) 방법
1. **Homebrew를 사용해 Docker 설치:**
   ```bash
   brew install --cask docker
   ```
2. **Docker Desktop 실행:**
   - 애플리케이션 폴더에서 Docker를 실행하거나 터미널에서 Docker Desktop을 시작합니다.

3. **Docker 버전 확인:**
   ```bash
   docker --version
   ```

## 설치(접속) 확인
아래 명령어를 실행하여 Docker 버전 확인:
```bash
docker --version
```

출력 예시:
```
Docker version 20.10.24, build abc123
```

![접속 화면 설명](Docker.png)

## 주의 사항
- Docker Desktop을 실행하기 전에 **Docker Daemon**이 시작되었는지 확인하세요.
- macOS에서 Docker를 실행하려면 Virtualization이 활성화되어 있어야 합니다.
- 무료 버전의 Docker Desktop은 비상업적 사용에 적합하며, 상업적 사용 시 라이선스를 확인하세요.

## 관련 URL
[Docker 공식 웹사이트](https://www.docker.com)
