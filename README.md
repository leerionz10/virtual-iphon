# Virtual iPhone — 웹 기반 가상 스마트폰

휴대폰 브라우저에서 실행할 수 있는 iOS 스타일의 가상 스마트폰 데모입니다.

## 포함된 기능
- 잠금 화면, 시계, 홈 화면, 앱 아이콘, 제어 센터
- 가상 메시지 대화 목록과 대화방
- 연락처 추가/삭제 및 연락처에서 대화 시작
- 상단 알림 배너와 잠금 화면/홈 화면 알림 카드
- 사진 가져오기, 사진을 배경화면으로 설정
- 메모 작성·수정·삭제 및 자동 저장
- 계산기, 시계, 스톱워치, 타이머
- 테마 배경, 제목, 강조 색상, 밝기 UI 변경
- JSON 데이터 백업/복원
- 브라우저 안에서 localStorage로 저장

## 실행
1. ZIP 압축을 풉니다.
2. `index.html`을 브라우저에서 열어 테스트합니다.
3. 권장: VS Code + Live Server 또는 로컬 정적 서버로 실행합니다.

## Vercel 배포
1. GitHub에 새 저장소를 만듭니다.
2. `index.html`, `style.css`, `app.js`를 저장소 최상위에 올립니다.
3. Vercel에서 Add New → Project를 선택하고 저장소를 연결합니다.
4. Framework Preset은 Other, Build Command는 비워 두고 Output Directory는 `.` 로 설정한 뒤 Deploy합니다.

## Cloudflare Pages 배포
1. GitHub 저장소에 파일 3개를 올립니다.
2. Cloudflare 대시보드 → Workers & Pages → Create → Pages → Connect to Git을 선택합니다.
3. Framework preset은 None, Build command는 비워 두고 Build output directory는 `/` 또는 저장소 루트로 지정합니다.
4. Deploy 후 제공된 `pages.dev` 주소로 접속합니다.

## 실제 기능과 시뮬레이션의 차이
이 프로젝트는 웹앱 내부에서 동작하는 시뮬레이션입니다.
- 메시지는 이 브라우저 안의 가상 대화로만 저장되며 SMS/iMessage를 보내지 않습니다.
- 알림 배너는 웹앱 화면 내부에 표시됩니다. 앱을 닫은 뒤에도 도착하는 푸시 알림은 구현하지 않았습니다.
- Wi-Fi, Bluetooth, 비행기 모드, 화면 밝기, 볼륨, 손전등은 실제 휴대폰 설정을 바꾸지 않습니다.
- 브라우저 앱은 주소를 새 탭으로 엽니다. 웹페이지를 앱 안에 임의로 임베드하지 않습니다.
- 사진과 설정은 현재 브라우저의 localStorage에 저장됩니다. 브라우저 데이터를 지우거나 다른 브라우저/기기를 쓰면 사라질 수 있습니다.
- 사진은 브라우저 저장 공간을 많이 쓸 수 있습니다. 중요한 데이터는 설정에서 JSON 백업을 내보내세요.
- 이 프로젝트는 iOS의 공식 복제품이 아니며 Apple의 시스템 앱/서비스와 연결되지 않습니다.

## 사용자화
- `app.js`: 초기 연락처/메모, 앱 기능과 동작
- `style.css`: 색상, 레이아웃, 애니메이션
- `index.html`: 홈 화면 앱과 구조
