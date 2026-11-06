# 따옴 변환 — Windows 설치와 자동 업데이트

[웹에서 사용하기](https://ttaom.kr/convert/#desktop) · [Windows 0.8.6 릴리스](https://github.com/bluezion/ttaom-convert-releases/releases/tag/v0.8.6)

현재 Windows 배포는 **코드 서명이 없는 미리보기**입니다. Windows에 확인되지 않은 게시자 경고가 표시될 수 있습니다.

## 처음 설치

1. [Microsoft 공식 Visual C++ x64 installer](https://aka.ms/vs/17/release/vc_redist.x64.exe)를 직접 다운로드하고 일반 설치 화면에서 Microsoft 게시자와 약관을 확인하세요. 14.44.35112 이상 또는 호환되는 새 버전이 필요합니다. 이미 호환 runtime이 있으면 다시 설치할 필요가 없습니다. 앱은 Microsoft runtime DLL과 installer를 번들하지 않습니다. embedded Python은 포함하되 그 폴더의 MSVC DLL은 제외합니다.
2. [0.8.6 Setup](https://github.com/bluezion/ttaom-convert-releases/releases/download/v0.8.6/LocalConvert.Desktop-win-Setup.exe)을 받아 [SHA-256 목록](https://github.com/bluezion/ttaom-convert-releases/releases/download/v0.8.6/SHA256SUMS.txt)을 대조해 설치하세요. 시스템 보안 설정을 끄는 절차는 제공하지 않습니다.

Setup SHA-256: `eb0207c04919fbd56e508621b61677fc4ee99dfb6d2529445d056158f685c1e4`.

## 이후 자동 업데이트

**0.8.6부터 자동 업데이트가 기본으로 켜져 있습니다.** 앱 시작 시 새 버전을 확인하고 다운로드합니다. 앱이 백그라운드이고 작업·웹 연결·저장하지 않은 입력/설정·열린 선택 창이 없을 때 적용하고 다시 시작합니다. 설정과 작업 기록, 저장한 결과는 유지합니다.

자동 업데이트를 끄려면 앱의 업데이트 화면에서 스위치를 끄세요. 직접 진행할 때는 **‘최신 버전 확인’ 후 ‘업데이트’ 한 번**으로 다운로드와 적용을 진행할 수 있습니다.

0.8.5 이하에는 이 기본 자동 동작이 없으므로 0.8.6으로 한 번 직접 업데이트하거나 새 Setup을 설치해야 합니다. 0.8.4는 업데이트 확인 오류가 있으므로 Setup을 직접 사용하세요. 이전 버전 파일은 변경하지 않고 보존합니다.

feed는 `https://github.com/bluezion/ttaom-convert-releases/releases/latest/download/releases.win.json`입니다. 버전별 package는 고정 이름으로 게시하며, draft 자산을 다시 받아 해시를 확인한 뒤 공개합니다. Windows 게시자 서명과 SHA-256은 서로 다른 검증 수단입니다.

## 검증 범위

새 통합 코드를 QA 전용 낮은 버전으로 별도 설치하여 실제 공개 0.8.6을 자동 다운로드·적용·재시작하는 전체 경로를 확인했습니다. foreground, 열린 Windows 파일 선택 창, 저장하지 않은 옵션이 있을 때 적용을 미루고, 안전한 background 상태에서 자동 적용하는 것을 확인했습니다. 자동 OFF와 수동 단일 버튼 경로, 설정·기록·원본/결과 파일의 해시 보존도 확인했습니다. QA 빌드는 공개하지 않았습니다.

검증 PC에는 Microsoft runtime 14.51.36247이 이미 설치돼 있습니다. runtime이 전혀 없는 깨끗한 PC의 Microsoft installer 설치·UAC·재시작 전체 경로를 검증했다는 뜻은 아닙니다. 정식 코드 서명·상용 검토 완료본도 아닙니다.

## 개인정보

선택한 파일, 파일 이름, 변환 결과와 로컬 연결 키는 인터넷 서버로 전송하지 않습니다. 파일 변환은 사용자의 기기에서 처리합니다. 업데이트와 선택 엔진 설치는 엔진 자산만 다운로드하며, 명시적으로 요청한 원격 URL 다운로드는 별도 화면에서 실행합니다.

이 저장소는 배포 안내와 설치/업데이트 자산 전용입니다. 비공개 앱 저장소·인증 정보는 게시하지 않으며 기존 따옴 캡처 앱 배포와 분리합니다.
