# 개발자 포트폴리오 웹사이트

개발한 앱과 서비스들을 모아놓은 개인 포트폴리오 웹사이트입니다.

## 기술 스택

- **React 19** - 최신 React 버전
- **TypeScript** - 타입 안정성
- **Vite** - 빠른 빌드 도구
- **Tailwind CSS** - 유틸리티 우선 CSS 프레임워크
- **다크/라이트 테마** - 자동 테마 전환 지원

## 주요 기능

✨ **반응형 디자인** - 모든 기기에서 완벽하게 작동
🌓 **다크/라이트 모드** - 사용자 선호도에 따라 자동 전환
📱 **모바일 최적화** - 모바일 우선 디자인
🚀 **빠른 로딩** - Vite를 통한 최적화된 빌드
🎨 **깔끔한 UI** - 현대적이고 미니멀한 디자인

## 프로젝트 구조

```
developer-portfolio-website/
├── components/          # React 컴포넌트
│   ├── Header.tsx      # 네비게이션 헤더
│   ├── Hero.tsx        # 메인 히어로 섹션
│   ├── Apps.tsx        # 앱 포트폴리오 섹션
│   ├── Support.tsx     # 지원/연락처 섹션
│   ├── Privacy.tsx     # 개인정보 처리방침
│   └── Footer.tsx      # 푸터
├── services/           # 서비스 로직
├── App.tsx            # 메인 앱 컴포넌트
├── index.tsx          # 엔트리 포인트
├── index.html         # HTML 템플릿
├── index.css          # 전역 스타일
├── types.ts           # TypeScript 타입 정의
└── vite.config.ts     # Vite 설정
```

## 로컬에서 실행하기

### 사전 요구사항
- Node.js (v18 이상 권장)
- npm 또는 yarn

### 설치 및 실행

1. **의존성 설치**
   ```bash
   cd developer-portfolio-website
   npm install
   ```

2. **개발 서버 실행**
   ```bash
   npm run dev
   ```
   브라우저에서 `http://localhost:5173` 접속

3. **프로덕션 빌드**
   ```bash
   npm run build
   ```
   빌드된 파일은 `dist/` 폴더에 생성됩니다.

4. **빌드 미리보기**
   ```bash
   npm run preview
   ```

## 커스터마이징 가이드

### 1. 개인 정보 수정

`components/Hero.tsx` 파일을 열어 다음을 수정하세요:
- 이름: "Suemin Hong" → 본인 이름
- 소개 문구: "Welcome to my digital space..." → 원하는 소개

### 2. 앱 정보 추가/수정

`components/Apps.tsx` 파일의 `placeholderApps` 배열을 수정:
```typescript
const placeholderApps: AppInfo[] = [
  {
    icon: <YourIcon />,
    name: '앱 이름',
    description: '앱 설명',
    storeUrl: 'https://apps.apple.com/...',
  },
  // 더 많은 앱 추가...
];
```

### 3. 색상 테마 변경

`index.html` 파일의 CSS 변수를 수정:
```css
:root {
  --color-background: #F2EFE9;
  --color-text-primary: #403732;
  --color-text-secondary: #736D66;
  /* ... */
}
```

### 4. 연락처 정보 수정

`components/Support.tsx`에서 이메일 주소를 변경하세요.

### 5. 소셜 링크 추가

`components/Footer.tsx`에서 소셜 미디어 링크를 수정하세요.

## 배포하기

이 웹사이트는 정적 사이트로 다양한 플랫폼에 무료로 배포할 수 있습니다:

### Vercel 배포 (권장)

1. [Vercel](https://vercel.com) 계정 생성
2. GitHub 저장소 연결
3. 자동 배포 완료!

**설정:**
- Build Command: `npm run build`
- Output Directory: `dist`
- Install Command: `npm install`

### Netlify 배포

1. [Netlify](https://netlify.com) 계정 생성
2. "New site from Git" 선택
3. 저장소 연결 및 설정:
   - Build command: `npm run build`
   - Publish directory: `dist`

### GitHub Pages 배포

1. 프로젝트를 GitHub에 푸시
2. `package.json`에 base 경로 추가:
   ```json
   {
     "scripts": {
       "build": "vite build --base=/repository-name/"
     }
   }
   ```
3. GitHub Settings → Pages → Source를 GitHub Actions로 설정
4. 빌드 후 `dist` 폴더를 `gh-pages` 브랜치에 푸시

### 커스텀 도메인 연결

대부분의 호스팅 서비스에서 커스텀 도메인을 쉽게 연결할 수 있습니다:
1. 도메인 구매 (예: Cloudflare, GoDaddy, Namecheap)
2. 호스팅 서비스의 DNS 설정 안내를 따라 설정
3. SSL 인증서 자동 발급 (대부분 무료)

## 환경 변수

Gemini API를 사용하는 경우, `.env.local` 파일을 생성하고 API 키를 추가하세요:
```
VITE_GEMINI_API_KEY=your_api_key_here
```

## 라이선스

이 프로젝트는 개인 포트폴리오 용도로 자유롭게 사용하실 수 있습니다.

## 문의

궁금한 점이 있으시면 이슈를 생성하거나 이메일로 연락주세요.

---

**Made with ❤️ by zziraengi**
