# 따옴 변환 — Windows 설치와 업데이트

[웹에서 변환하기](https://ttaom.kr/convert/#desktop) · [Windows 0.8.5 릴리스](https://github.com/bluezion/ttaom-convert-releases/releases/tag/v0.8.5)

현재 Windows 배포는 **코드 서명이 없는 미리보기**입니다. 앱과 Setup에 확인되지 않은 게시자 경고가 표시될 수 있습니다. 정식 코드 서명·상용 검토 완료본은 아닙니다.

## 처음 설치

1. **Microsoft runtime을 먼저 준비하세요.** [Microsoft 공식 Visual C++ x64 installer](https://aka.ms/vs/17/release/vc_redist.x64.exe)를 직접 다운로드하고 일반 설치 화면에서 Microsoft 게시자와 약관을 확인하세요. 14.44.35112 이상 또는 호환되는 새 버전이 필요합니다. 이미 호환 runtime이 있다면 다시 설치할 필요가 없습니다. 앱에는 MSVC runtime DLL이나 Microsoft installer가 포함돼 있지 않습니다. embedded Python 자체는 포함되며 그 폴더의 MSVC DLL만 제외했습니다.
2. [0.8.5 Setup](https://github.com/bluezion/ttaom-convert-releases/releases/download/v0.8.5/LocalConvert.Desktop-win-Setup.exe)을 다운로드하고 [SHA-256 목록](https://github.com/bluezion/ttaom-convert-releases/releases/download/v0.8.5/SHA256SUMS.txt)을 대조해 설치하세요. 시스템 보안 설정을 끄는 절차는 제공하지 않습니다.
3. 이후 앱은 시작할 때 업데이트를 자동 확인합니다. **다운로드와 적용·재시작은 앱의 업데이트 화면에서 사용자가 선택합니다.** 무인 자동 설치 방식은 아닙니다. 변환·녹화·엔진 설치 중 적용은 차단됩니다.

0.8.4는 SDK의 GitHub URL 자동 분류로 업데이트 확인이 실패하는 문제가 있어 0.8.5에서 명시적인 HTTP feed로 수정했습니다. **0.8.4 이하 사용자는 0.8.5 Setup을 한 번 직접 설치해야 합니다.** 이전 버전 파일은 변경하지 않고 보존합니다.

## 업데이트 경로와 검증 범위

업데이트 feed는 `https://github.com/bluezion/ttaom-convert-releases/releases/latest/download/releases.win.json`입니다. 버전별 패키지는 고정 이름으로 게시하고 기존 파일을 덮어쓰지 않습니다. draft에 업로드한 자산을 다시 받아 해시를 대조한 뒤 release 전체를 공개합니다. Windows 게시자 서명과 파일 SHA-256은 서로 다른 검증 수단입니다.

runtime 14.51.36247이 설치된 Windows에서 새 설치, 실제 이미지·PDF·영상 변환, 업데이트 다운로드/해시/적용/재시작과 데이터 보존을 시험합니다. runtime이 전혀 없는 깨끗한 PC에서 Microsoft installer 설치·약관·재시작 경로까지 검증한 것은 아닙니다. 개발 도구 사용 자격·특허 등 상용 검토가 완료됐다는 의미도 아닙니다.

## 개인정보

선택한 파일, 파일 이름, 변환 결과와 로컬 연결 키는 인터넷 서버로 전송하지 않습니다. 파일 변환은 사용자의 기기에서 처리합니다. 업데이트와 선택 엔진 설치는 고정 엔진 자산만 다운로드합니다. 사용자가 명시적으로 요청한 원격 URL 다운로드는 별도 화면에서 실행합니다.

이 저장소는 배포 안내와 설치/업데이트 자산 전용입니다. 비공개 앱 저장소·인증 정보는 게시하지 않으며 기존 따옴 캡처 앱의 배포와 분리합니다.
