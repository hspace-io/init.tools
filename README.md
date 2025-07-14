# 🔧 해킹 도구 설치 가이드

초보 해커들이 실습에 필요한 도구들을 손쉽게 설치하고 활용할 수 있도록 이 가이드를 제공합니다. 도구별 설명, 설치법, 주요 기능을 중심으로 정리했습니다.

---

## 📁 디렉토리 구조

- `CORE/`: 개발 환경 설정에 필요한 기본 도구들 (코드 에디터, 언어, 패키지 매니저 등)
- `Software hacking/`: 리버스 엔지니어링, 포렌식, 분석 도구 등 전문 해킹 도구 모음

---

## 📘 도구 분류별 전체 요약 (주요 기능 제외)

| 분류 | 도구명 | 지원 OS (M: macOS / W: Windows / L: Linux) | 권장 설치 |
|------|--------|---------------------------------------------|------------|
| CORE | [Code Editing Tools](CORE/Code%20Editing%20Tools.md) |  |  |
| CORE | [Compiler](CORE/Compiler.md) |  |  |
| CORE | [Language](CORE/Language.md) |  |  |
| CORE | [Package Management Tools](CORE/Package%20Management%20Tools.md) |  |  |
| CORE | [Virtual Enviroment](CORE/Virtual%20Enviroment.md) |  |  |
| Software hacking | [010Editor](Software%20hacking/010Editor.md) | M W |  |
| Software hacking | [ADB (Android Debug Bridge)](Software%20hacking/ADB%20(Android%20Debug%20Bridge).md) |  |  |
| Software hacking | [Android Studio AVD](Software%20hacking/Android%20Studio%20AVD.md) | M W L |  |
| Software hacking | [Autopsy](Software%20hacking/Autopsy.md) | M W L |  |
| Software hacking | [BrowsingHistoryView](Software%20hacking/BrowsingHistoryView.md) | W |  |
| Software hacking | [Burp Suite](Software%20hacking/Burp%20Suite.md) | M W L |  |
| Software hacking | [Cheat Engine](Software%20hacking/Cheat%20Engine.md) | M W |  |
| Software hacking | [Curl](Software%20hacking/Curl.md) | M W L |  |
| Software hacking | [CyberChef](Software%20hacking/CyberChef.md) |  |  |
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
| Software hacking | [Remix IDE](Software%20hacking/Remix%20IDE.md) |  |  |
| Software hacking | [RustScan](Software%20hacking/RustScan.md) | M W L |  |
| Software hacking | [SHODAN](Software%20hacking/SHODAN.md) |  |  |
| Software hacking | [Sage Math](Software%20hacking/Sage%20Math.md) | M W L |  |
| Software hacking | [Volatility](Software%20hacking/Volatility.md) | M W L |  |
| Software hacking | [Webhook Tester](Software%20hacking/Webhook%20Tester.md) |  |  |
| Software hacking | [Windbg (Windows Debugger)](Software%20hacking/Windbg%20(Windows%20Debugger).md) | W |  |
| Software hacking | [Wireshark](Software%20hacking/Wireshark.md) | M W |  |
| Software hacking | [Z3 Solver](Software%20hacking/Z3%20Solver.md) | M W L |  |
| Software hacking | [anvil](Software%20hacking/anvil.md) |  |  |
| Software hacking | [censys](Software%20hacking/censys.md) |  |  |
| Software hacking | [dnSpy](Software%20hacking/dnSpy.md) | W |  |
| Software hacking | [ether.js](Software%20hacking/ether.js.md) |  |  |
| Software hacking | [foundry](Software%20hacking/foundry.md) | M W L |  |
| Software hacking | [gdb](Software%20hacking/gdb.md) | L |  |
| Software hacking | [gef](Software%20hacking/gef.md) | L |  |
| Software hacking | [hardhat](Software%20hacking/hardhat.md) |  |  |
| Software hacking | [nc (netcat)](Software%20hacking/nc%20(netcat).md) | M W L |  |
| Software hacking | [ngrok](Software%20hacking/ngrok.md) |  |  |
| Software hacking | [postman](Software%20hacking/postman.md) | M W L |  |
| Software hacking | [pwndbg](Software%20hacking/pwndbg.md) | L |  |
| Software hacking | [pwntools](Software%20hacking/pwntools.md) | M W L |  |
| Software hacking | [rp++](Software%20hacking/rp++.md) | M W L |  |
| Software hacking | [sqlmap](Software%20hacking/sqlmap.md) | M W L |  |
| Software hacking | [web3.js](Software%20hacking/web3.js.md) |  |  |
| Software hacking | [x64dbg](Software%20hacking/x64dbg.md) | W |  |
