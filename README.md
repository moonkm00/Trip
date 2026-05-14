# ✈️ Trip Project (여행 정보 공유 및 커뮤니티 플랫폼)

사용자들에게 국내외 여행 정보, 축제 정보 및 커뮤니티 공간을 제공하는 웹 애플리케이션 프로젝트입니다.

## 🚀 주요 기능

### 1. 사용자 인증 및 관리
- **로그인/회원가입**: 소셜 로그인(카카오, 네이버) 및 일반 로그인 지원. bcrypt를 통한 비밀번호 암호화.
- **마이페이지**: 프로필 수정, 프로필 이미지 업로드, 좋아요 리스트 조회, 작성한 리뷰/게시글/Q&A 관리.
- **비밀번호 찾기**: 이메일 인증을 통한 임시 비밀번호 발급 및 재설정.

### 2. 여행 및 축제 정보 (Travel & Festival)
- **정보 조회**: TV 속 여행지(`trip_tv_info`) 및 축제(`trip_fs_info`) 상세 정보 제공.
- **검색 기능**: 제목 키워드 기반의 통합 검색.
- **리뷰 시스템**: 각 여행지/축제별 별점 및 텍스트 리뷰 작성 기능.
- **좋아요(찜)**: 선호하는 장소 찜하기 및 통계 기반 'Best' 항목 노출.

### 3. 커뮤니티 및 소통
- **자유 게시판**: 사용자 간 여행 후기 및 팁 공유 (이미지 업로드, 댓글 기능 포함).
- **Q&A**: 1:1 문의 시스템 (비밀글 설정 기능).

### 4. 관리자 기능 (Admin)
- **대시보드**: 사용자 통계, 게시글 조회수 및 좋아요 랭킹 시각화.
- **회원 및 콘텐츠 관리**: 전체 사용자 목록 조회, 부적절한 게시글/리뷰 삭제 및 데이터 관리.

---

## 🛠 기술 스택

### Frontend
- **Framework**: Vue 3
- **State Management**: Vuex (with vuex-persistedstate)
- **UI Framework**: Vuetify, Bootstrap, Quasar
- **Charts/Visualization**: Chart.js, D3.js
- **Network**: Axios
- **Other**: Splidejs (Slider), Sweetalert2 (Alerts)

### Backend
- **Runtime**: Node.js
- **Framework**: Express
- **Database**: MySQL (mysql2)
- **Security**: bcrypt (Password hashing)
- **Mail**: Nodemailer (Email service)
- **File Upload**: Multer

---

## 📂 프로젝트 구조

```text
Trip/
├── node-back/          # Express 백엔드 서버
│   ├── routes/         # API 라우터 (auth, trip, admin, qna 등)
│   ├── myImg/          # 업로드된 이미지 저장소
│   ├── app.js          # 서버 진입점 (Port: 3000)
│   ├── sql.js          # SQL 쿼리 모음
│   └── db.js           # DB 연결 설정
├── vue-front/          # Vue 3 프론트엔드
│   ├── src/
│   │   ├── view/       # 페이지 컴포넌트 (main, login, board 등)
│   │   ├── components/ # 공통 UI 컴포넌트
│   │   ├── layout/     # 페이지 레이아웃
│   │   ├── store/      # Vuex 상태 관리
│   │   └── main.js     # 프론트엔드 진입점
│   └── package.json    # 프론트엔드 의존성 설정
└── README.md
```

---

## 🏃 시작하기

### 1. Backend 설정 및 실행
```bash
cd node-back
npm install
# db.js 파일에서 MySQL 연결 정보를 설정해야 합니다.
npm start
```

### 2. Frontend 설정 및 실행
```bash
cd vue-front
npm install
npm run serve
```
- 접속 주소: `http://localhost:8080`

---

## 📝 참고 사항
- 백엔드 서버는 `http://localhost:3000`에서 실행됩니다.
- 프론트엔드는 `http://localhost:8080`에서 실행되며, CORS 설정이 백엔드(`app.js`)에 적용되어 있습니다.
