# The Themis — 다운로드 사이트

GitHub Pages로 배포하는 정적 페이지. 설치 파일은 저장소에 넣지 않고 **Releases**에 올린다.

- 페이지: `index.html` + `assets/` (배경 · 엠블럼 · 글꼴)
- 다운로드 링크는 항상 최신 릴리스를 가리킨다
  - Windows: `releases/latest/download/TheThemis-WebSetup.exe`
  - Android: `releases/latest/download/TheThemis.apk`
- 새 버전 올리기: Releases에서 새 릴리스를 만들고 **같은 파일 이름**으로 첨부 → 페이지 수정 없이 링크가 새 파일을 받는다

```
gh release create v1.0 TheThemis-WebSetup.exe TheThemis.apk --title "The Themis 1.0"
```

## 배포 (페이지)
주소: **https://thethemis.pages.dev** (Cloudflare Pages 프로젝트 `thethemis`). 저장소에 올린 파일만 내보낸다 — 로컬 `_release/`의 설치 파일(APK 67MB)은 Pages 한도(25MB)를 넘으니 함께 올리면 안 된다.

```
rm -rf ../.site-deploy && mkdir ../.site-deploy && git archive HEAD | tar -x -C ../.site-deploy
npx wrangler pages deploy ../.site-deploy --project-name thethemis --branch main
```
