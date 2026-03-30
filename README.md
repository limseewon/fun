# 사주 명리 — AI 사주 해석 서비스

Anthropic Claude API를 활용한 명리학 사주 해석 웹서비스.

## 파일 구조

```
saju-app/
├── api/
│   └── saju.js        # Vercel Edge Function (API 키 보관)
├── public/
│   └── index.html     # 프론트엔드
├── vercel.json        # Vercel 설정
└── README.md
```

## 배포 방법 (Vercel)

### 1단계 — GitHub에 올리기

```bash
git init
git add .
git commit -m "init"
git remote add origin https://github.com/YOUR_USERNAME/saju-app.git
git push -u origin main
```

### 2단계 — Vercel 연결

1. [vercel.com](https://vercel.com) 접속 → GitHub 로그인
2. "Add New Project" → GitHub 저장소 선택
3. Import 클릭

### 3단계 — API 키 환경변수 설정

Vercel 프로젝트 설정에서:
- Settings → Environment Variables
- 이름: `ANTHROPIC_API_KEY`
- 값: `sk-ant-...` (Anthropic Console에서 발급)
- 저장 후 **Redeploy**

### 완료

배포 후 `https://your-project.vercel.app` 으로 접속하면 끝.
사용자는 API 키 입력 없이 바로 사용 가능.

## 로컬 테스트

```bash
npm i -g vercel
vercel dev
```

환경변수는 `.env` 파일에:
```
ANTHROPIC_API_KEY=sk-ant-...
```
