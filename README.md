# 🔧 해킹 도구 설치 가이드

초보 해커들이 실습에 필요한 도구들을 손쉽게 설치하고 활용할 수 있도록 이 가이드를 제공합니다. 도구별 설명, 설치법, 주요 기능을 중심으로 정리했습니다.

---

## 🚀 시작하기

이 저장소는 해킹 및 보안 실습에 필요한 다양한 도구들의 설치 방법과 기본적인 사용 가이드를 제공합니다. 각 도구는 개별 Markdown 파일로 정리되어 있으며, 필요에 따라 설치 및 활용할 수 있습니다.

### 📦 저장소 클론

```bash
git clone https://github.com/hspace-io/init.tools.git
cd init.tools
git checkout ver1
```

### 📖 도구 사용 가이드

각 도구에 대한 상세 정보는 해당 도구의 Markdown 파일을 참조하십시오. 파일은 `CORE/` 또는 `Software hacking/` 디렉토리에 분류되어 있습니다.

예시:

- **Code Editing Tools**: `CORE/Code Editing Tools.md`
- **Burp Suite**: `Software hacking/Burp Suite.md`

각 파일에는 다음과 같은 내용이 포함되어 있습니다:

- **설명**: 도구의 목적과 주요 기능에 대한 간략한 설명
- **설치 영역**: 도구가 설치되는 일반적인 경로
- **주요 기능**: 도구가 제공하는 핵심 기능 목록
- **설치 방법**: 운영체제별 설치 지침
- **간단 가이드**: 도구의 기본적인 사용 방법 및 예시
- **관련 URL**: 공식 웹사이트, 문서, GitHub 저장소 등 추가 정보 링크

---

## 📁 디렉토리 구조

- `CORE/`: 개발 환경 설정에 필요한 기본 도구들 (코드 에디터, 언어, 패키지 매니저 등)
- `Software hacking/`: 리버스 엔지니어링, 포렌식, 분석 도구 등 전문 해킹 도구 모음
- `TAG/`: 태그별 도구 정리
- `img/`: 문서에 사용되는 이미지 파일

---

## 📘 도구 분류별 전체 요약

| 분류 | 도구명 | 지원 OS (M: macOS / W: Windows / L: Linux) | 권장 설치 |
|------|--------|---------------------------------------------|------------|
| CORE | [Code Editing Tools](CORE/Code%20Editing%20Tools.md) | M W L |  |
| CORE | [Compiler](CORE/Compiler.md) | M W L |  |
| CORE | [Language](CORE/Language.md) | M W L |  |
| CORE | [Package Management Tools](CORE/Package%20Management%20Tools.md) | M W L |  |
| CORE | [Virtual Enviroment](CORE/Virtual%20Enviroment.md) | M W L |  |
| Software hacking | [010Editor](Software%20hacking/010Editor.md) | M W |  |
| Software hacking | [ADB (Android Debug Bridge)](Software%20hacking/ADB%20(Android%20Debug%20Bridge).md) | M W L |  |
| Software hacking | [Android Studio AVD](Software%20hacking/Android%20Studio%20AVD.md) | M W L |  |
| Software hacking | [Autopsy](Software%20hacking/Autopsy.md) | M W L |  |
| Software hacking | [BrowsingHistoryView](Software%20hacking/BrowsingHistoryView.md) | W |  |
| Software hacking | [Burp Suite](Software%20hacking/Burp%20Suite.md) | M W L |  |
| Software hacking | [Cheat Engine](Software%20hacking/Cheat%20Engine.md) | M W |  |
| Software hacking | [Curl](Software%20hacking/Curl.md) | M W L |  |
| Software hacking | [CyberChef](Software%20hacking/CyberChef.md) | M W L |  |
| Software hacking | [DB Browser for SQLite](Software%20hacking/DB%20Browser%20for%20SQLite.md) | M W L |  |
| Software hacking | [DIE (Detect It Easy)](Software%20hacking/DIE%20(Detect%20It%20Easy).md) | M W L |  |
| Software hacking | [EnCase (유료)](Software%20hacking/EnCase%20(유료).md) | M W L |  |
| Software hacking | [ExifTool](Software%20hacking/ExifTool.md) | M W L |  |
| Software hacking | [FRIDA](Software%20hacking/FRIDA.md) | M W L |  |
| Software hacking | [FTK Imager](Software%20hacking/FTK%20Imager.md) | W |  |
| Software hacking | [Fiddler](Software%20hacking/Fiddler.md) | M W L |  |
| Software hacking | [GHIDRA](Software%20hacking/GHIDRA.md) | M W L |  |
| Software hacking | [Hex Fiend](Software%20hacking/Hex%20Fiend.md) | M |  |
| Software hacking | [HxD (Freeware Hex Editor and Disk Editor)](Software%20hacking/HxD%20(Freeware%20Hex%20Editor%20and%20Disk%20Editor).md) | W |  |
| Software hacking | [IDA Free](Software%20hacking/IDA%20Free.md) | M W L |  |
| Software hacking | [JADX](Software%20hacking/JADX.md) | M W L |  |
| Software hacking | [LNK Parser (보류 -> 종류가 다양함)](Software%20hacking/LNK%20Parser%20(보류%20->%20종류가%20다양함).md) | W |  |
| Software hacking | [NOX](Software%20hacking/NOX.md) | W |  |
| Software hacking | [NTFS Log Tracker](Software%20hacking/NTFS%20Log%20Tracker.md) | W |  |
| Software hacking | [Nmap](Software%20hacking/Nmap.md) | M W L |  |
| Software hacking | [NumPy](Software%20hacking/NumPy.md) | M W L |  |
| Software hacking | [OWASP ZAP (Zed Attack Proxy)](Software%20hacking/OWASP%20ZAP%20(Zed%20Attack%20Proxy).md) | M W L |  |
| Software hacking | [QEMU](Software%20hacking/QEMU.md) | M W L |  |
| Software hacking | [REGA](Software%20hacking/REGA.md) | W |  |
| Software hacking | [ROP Gadget](Software%20hacking/ROP%20Gadget.md) | M W L |  |
| Software hacking | [Remix IDE](Software%20hacking/Remix%20IDE.md) | M W L |  |
| Software hacking | [RustScan](Software%20hacking/RustScan.md) | M W L |  |
| Software hacking | [SHODAN](Software%20hacking/SHODAN.md) | M W L |  |
| Software hacking | [Sage Math](Software%20hacking/Sage%20Math.md) | M W L |  |
| Software hacking | [Volatility](Software%20hacking/Volatility.md) | M W L |  |
| Software hacking | [Webhook Tester](Software%20hacking/Webhook%20Tester.md) | M W L |  |
| Software hacking | [Windbg (Windows Debugger)](Software%20hacking/Windbg%20(Windows%20Debugger).md) | W |  |
| Software hacking | [Wireshark](Software%20hacking/Wireshark.md) | M W L |  |
| Software hacking | [Z3 Solver](Software%20hacking/Z3%20Solver.md) | M W L |  |
| Software hacking | [anvil](Software%20hacking/anvil.md) | M W L |  |
| Software hacking | [censys](Software%20hacking/censys.md) | M W L |  |
| Software hacking | [dnSpy](Software%20hacking/dnSpy.md) | W |  |
| Software hacking | [ether.js](Software%20hacking/ether.js.md) | M W L |  |
| Software hacking | [foundry](Software%20hacking/foundry.md) | M W L |  |
| Software hacking | [gdb](Software%20hacking/gdb.md) | L |  |
| Software hacking | [gef](Software%20hacking/gef.md) | L |  |
| Software hacking | [hardhat](Software%20hacking/hardhat.md) | M W L |  |
| Software hacking | [nc (netcat)](Software%20hacking/nc%20(netcat).md) | M W L |  |
| Software hacking | [ngrok](Software%20hacking/ngrok.md) | M W L |  |
| Software hacking | [postman](Software%20hacking/postman.md) | M W L |  |
| Software hacking | [pwndbg](Software%20hacking/pwndbg.md) | L |  |
| Software hacking | [pwntools](Software%20hacking/pwntools.md) | M W L |  |
| Software hacking | [rp++](Software%20hacking/rp++.md) | M W L |  |
| Software hacking | [sqlmap](Software%20hacking/sqlmap.md) | M W L |  |
| Software hacking | [web3.js](Software%20hacking/web3.js.md) | M W L |  |
| Software hacking | [x64dbg](Software%20hacking/x64dbg.md) | W |  |

---

## 🏷️ 태그 가이드

`TAG/TAGS.md` 파일에는 각 도구에 적용된 태그 목록과 그 의미가 정의되어 있습니다. 이를 통해 특정 분야(예: `forensic`, `web_security`) 또는 운영체제(`windows`, `mac`, `linux`)에 해당하는 도구를 쉽게 찾을 수 있습니다.

---

## 🤝 기여 방법

이 저장소에 새로운 도구를 추가하거나 기존 내용을 개선하는 데 기여하고 싶으시다면, 다음 절차를 따르십시오:

1.  저장소를 포크(Fork)합니다.
2.  새로운 브랜치를 생성합니다 (`git checkout -b feature/your-feature-name`).
3.  변경 사항을 커밋합니다 (`git commit -m 'feat: Add new tool X'`).
4.  원격 저장소에 푸시합니다 (`git push origin feature/your-feature-name`).
5.  풀 리퀘스트(Pull Request)를 생성합니다.

---
