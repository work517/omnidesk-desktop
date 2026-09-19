# OmniDesk for Windows

**세상 모든 파일 형식을 하나의 데스크톱에서. — Every file format, one desktop.**

[**omnidesk.win**](https://omnidesk.win) 의 윈도우 앱을 내려받는 곳입니다.
**325종**의 문서·이미지·오디오·영상·전자책·압축·CAD·폰트·데이터 형식을
서로 변환하고, 회사별로 격리된 드라이브에 보관합니다.

> 이 저장소는 **내려받기 전용**입니다. 소스는 비공개이고, 여기에는 서명된
> 설치 파일만 올라옵니다.
> This repository hosts **downloads only** — signed Windows installers.
> Product, docs and pricing live at **<https://omnidesk.win>**.

---

## 내려받기 · Download

[**▶ 최신 릴리스 받기 / Latest release**](https://github.com/work517/omnidesk-desktop/releases/latest)
· [설치 안내 (한국어)](https://omnidesk.win/ko/download/)
· [Install guide (English)](https://omnidesk.win/en/download/)

| 파일 | 쓰임 | What it is |
|---|---|---|
| `OmniDesk-Windows-Setup.exe` | 설치본 — 시작 메뉴에 등록됩니다 | Installer, adds a Start-menu entry |
| `OmniDesk-Windows-Portable.exe` | 무설치 실행본 — 두 번 누르면 바로 실행 | Portable, just double-click |
| `*.sha256` | 무결성 확인용 | Checksums |

설치는 사용자 폴더에만 이뤄지고 관리자 권한을 묻지 않습니다.
Windows 10 / 11 (64-bit).

### 코드 서명 · Code signing

두 파일 모두 **PROJECTTEAMFORYOU** 이름으로 서명되어 있습니다.
파일 속성 → *디지털 서명* 탭에서 직접 확인하실 수 있습니다.
Both binaries are Authenticode-signed as **PROJECTTEAMFORYOU**; check the
*Digital Signatures* tab in file properties.

내려받은 파일이 올라온 그대로인지 확인하려면 (PowerShell):

```powershell
Get-FileHash .\OmniDesk-Windows-Setup.exe -Algorithm SHA256
# 옆에 받은 .sha256 파일의 값과 같아야 합니다
```

### "Windows에서 PC를 보호했습니다" 창이 뜬다면

SmartScreen 은 서명과 별개로 *이 게시자의 파일이 얼마나 많이, 얼마나 오래
문제 없이 실행됐는가* 를 봅니다. 서명을 시작한 지 얼마 되지 않아 그 이력이
아직 쌓이는 중입니다.

1. 브라우저가 "일반적으로 다운로드되지 않는 파일입니다" 라고 하면 → **유지**(Chrome) / **계속**(Edge)
2. 받은 파일을 두 번 누릅니다
3. 파란 창에서 **게시자가 `PROJECTTEAMFORYOU` 인지 확인**하고 → **추가 정보** → **실행**

게시자 이름을 확인하는 것이 진짜 검증 수단입니다.
*If SmartScreen warns: click **More info** → **Run**, after confirming the
publisher reads `PROJECTTEAMFORYOU`. The prompt fades as download reputation
accrues.*

---

## 무엇을 하는 앱인가 · What it does

- **325종 형식 변환** — 직접 지원하지 않는 조합도 중간 형식을 거쳐 자동으로
  이어집니다 (`dwg → dxf → png`). 변환 그래프가 가장 손실이 적은 경로를 찾습니다.
  *325 formats, routed automatically through intermediate formats when no
  direct converter exists.*
- **회사 드라이브** — 회사별로 격리된 저장소. 팀원끼리 폴더를 공유합니다.
  *Per-company isolated drive.*
- **12개 언어** — 한국어 · English · 日本語 · 中文 · Español · Português ·
  Français · Deutsch · Русский · العربية · Tiếng Việt · Bahasa Indonesia
- **웹으로도** — 설치하지 않고 브라우저에서 바로 쓸 수 있습니다: <https://app.omnidesk.win>

자세한 형식 목록과 요금은 홈페이지에 있습니다 —
[형식 전체 보기](https://omnidesk.win/ko/formats/) ·
[요금](https://omnidesk.win/ko/pricing/) ·
[보안](https://omnidesk.win/ko/security/) ·
[API](https://omnidesk.win/ko/api/)

### 다른 곳에서 쓰기 · Beyond the desktop

| | |
|---|---|
| 웹 앱 | <https://app.omnidesk.win> |
| REST API | <https://omnidesk.win/en/api/> |
| MCP 서버 (Claude 등 AI 도구에서 변환) | [`omnidesk-mcp`](https://pypi.org/project/omnidesk-mcp/) — `uvx omnidesk-mcp` |

---

## 언어별 홈페이지 · The site in your language

[한국어](https://omnidesk.win/ko/) ·
[English](https://omnidesk.win/en/) ·
[日本語](https://omnidesk.win/ja/) ·
[中文](https://omnidesk.win/zh/) ·
[Español](https://omnidesk.win/es/) ·
[Português](https://omnidesk.win/pt/) ·
[Français](https://omnidesk.win/fr/) ·
[Deutsch](https://omnidesk.win/de/) ·
[Русский](https://omnidesk.win/ru/) ·
[العربية](https://omnidesk.win/ar/) ·
[Tiếng Việt](https://omnidesk.win/vi/) ·
[Bahasa Indonesia](https://omnidesk.win/id/)

---

## 문의 · 약관

- 문의 · Support — **projectteamforyou@gmail.com**
- [개인정보처리방침 / Privacy policy](https://omnidesk.win/ko/privacy/)
- [이용약관 / Terms of service](https://omnidesk.win/ko/terms/)
- [환불정책 / Refund policy](https://omnidesk.win/ko/refund/)

버그나 요청은 **[Issues](https://github.com/work517/omnidesk-desktop/issues)**
에 남겨 주세요. 어떤 파일을 무엇으로 바꾸려 했는지, 앱 버전, 윈도우 판번호를
함께 적어 주시면 빠릅니다.
