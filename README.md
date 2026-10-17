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
