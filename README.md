# KB It's Your Life - 4팀 프로젝트

가계부 및 자산 관리 서비스를 위한 웹 애플리케이션입니다. Vue.js를 기반으로 하며, JSON Server를 백엔드로 활용하여 위시리스트, 예산 관리, 대시보드 등의 기능을 제공합니다.

## 🛠️ 기술 스택

- **Frontend**: Vue 3, Vite, Pinia, Vue Router, Axios
- **Backend**: JSON Server (Mock API)
- **Server**: Express (이미지 업로드용)
- **Tools**: Concurrently (프론트/백엔드 동시 실행)

## 📂 프로젝트 구조

```text
.
├── db.json                # JSON Server 데이터베이스
├── server.js              # 이미지 업로드 서버 (Express)
├── index.html             # 메인 HTML
├── vite.config.js         # Vite 설정 파일
├── public/                # 정적 자산 (아이콘 등)
└── src/
    ├── main.js            # 진입점
    ├── App.vue            # 메인 컴포넌트
    ├── api/               # API 통신 (purchase, wishlist 등)
    ├── components/
    │   └── common/        # 공용 컴포넌트 (Header, Sidebar)
    ├── pages/             # 페이지 단위 컴포넌트
    │   ├── auth/          # 인증 (로그인, 회원가입, 마이페이지)
    │   ├── budget/        # 예산 관리
    │   ├── dashboard/     # 대시보드
    │   ├── transaction/   # 거래 내역
    │   └── Wishlist/      # 위시리스트
    ├── router/            # Vue Router 설정
    └── utils/             # 공통 유틸리티 (인증 체크 등)
```

## 🚀 시작하기

### 1. 의존성 설치

프로젝트 루트 디렉토리에서 아래 명령어를 실행하여 필요한 패키지를 설치합니다.

```bash
npm install
```

### 2. 프로젝트 실행

프론트엔드, 백엔드(JSON Server), 업로드 서버를 한 번에 실행합니다.

```bash
npm run dev
```

- **Frontend**: [http://localhost:5173](http://localhost:5173) (기본값)
- **JSON Server**: [http://localhost:3000](http://localhost:3000)
- **Upload Server**: `server.js`에서 설정된 포트로 실행

### 3. 스크립트 상세 설명

- `npm run frontend`: Vite 개발 서버만 실행
- `npm run backend`: JSON Server(포트 3000) 실행
- `npm run upload`: `server.js` 실행 (이미지 업로드 처리)
- `npm run build`: 프로덕션 빌드 생성

## ✅ 주요 기능

- **대시보드**: 전체 자산 및 예산 현황 시각화
- **거래 내역**: 수입/지출 내역 관리
- **예산 관리**: 월별 목표 예산 설정 및 대비 확인
- **위시리스트**: 목표 구매 항목 관리
- **인증 시스템**: 회원가입, 로그인, 마이페이지 관리
