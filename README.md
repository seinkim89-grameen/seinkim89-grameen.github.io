# Sein Kim 홈페이지 — 올리기 & 구글 검색 등록 가이드

## 파일 구성
- `index.html` — 홈페이지 본체 (논문 목록 포함, 한 페이지)
- `robots.txt`, `sitemap.xml` — 구글 검색 로봇용 안내 파일
- `.nojekyll` — GitHub Pages 설정용 빈 파일 (지우지 마세요)
- `profile.jpg` — **직접 추가**: 프로필 사진을 이 이름으로 넣으면 자동으로 표시됩니다 (세로 4:5 비율 권장)

---

## 1단계. GitHub Pages에 올리기 (약 10분)

1. https://github.com 가입 (이미 있으면 로그인)
2. 오른쪽 위 **+ → New repository**
   - Repository name: **`seinkim89-grameen.github.io`**
   - Public 선택 → **Create repository**
3. 생성된 페이지에서 **uploading an existing file** 클릭 → 이 폴더의 파일을 모두 끌어다 놓기 → **Commit changes**
   - `.nojekyll`은 숨김 파일이라 안 보일 수 있어요. 없어도 사이트는 동작합니다.
4. 1~2분 뒤 `https://seinkim89-grameen.github.io` 로 접속하면 사이트가 열립니다.


---

## 2단계. 구글 검색에 나오게 하기

### ① Google Search Console 등록 (가장 중요)
1. https://search.google.com/search-console 접속 → **속성 추가**
2. **URL 접두어** 선택 → `https://seinkim89-grameen.github.io/` 입력
3. 확인 방법 중 **HTML 태그** 선택 → `<meta name="google-site-verification" content="...">` 복사
4. `index.html`에서 아래 줄을 찾아 주석을 풀고 코드 붙여넣기:
   ```html
   <!-- <meta name="google-site-verification" content="PASTE_CODE_HERE"> -->
   ```
   → `<meta name="google-site-verification" content="복사한코드">`
5. GitHub에 수정한 index.html 다시 올린 뒤 Search Console에서 **확인**
6. 왼쪽 메뉴 **Sitemaps** → `sitemap.xml` 입력 → 제출
7. 상단 검색창에 사이트 주소 입력 → **색인 생성 요청**

보통 며칠~2주 안에 "Sein Kim", "김세인 Harvard" 같은 검색어에 나오기 시작합니다.

### ② 링크 늘리기 (검색 순위를 올리는 데 가장 효과적)
구글은 **다른 곳에서 링크가 걸린 사이트**를 더 신뢰합니다.
- **기존 Google Sites 첫 화면**에 "새 홈페이지로 이동했습니다 → https://seinkim89-grameen.github.io" 링크 추가 (기존 사이트는 지우지 말고 유지)
- LinkedIn 프로필 → 연락처 정보 → 웹사이트에 추가
- Google Scholar 프로필 → 홈페이지 항목에 추가
- ORCID, 소속 기관 프로필 페이지, 이메일 서명에도 추가

### ③ 이미 들어가 있는 설정
- 제목/설명 메타태그: "Sein Kim (김세인) | Health Systems & Health Economics Researcher"
- 영문·한글 이름 모두 포함 → 두 이름 모두로 검색 가능
- 구조화 데이터(schema.org Person / ScholarlyArticle): 이름, 소속, 연구 분야, 논문 목록을 구글이 이해할 수 있는 형태로 포함
- 논문 목록이 HTML에 직접 들어가 있어 구글이 바로 읽을 수 있음

---

## 나중에 수정할 때
- 텍스트 수정: GitHub에서 `index.html` 열기 → 연필 아이콘 → 수정 → Commit
- 새 논문 추가: `<ol>` 안의 `<li>…</li>` 블록 하나를 복사해서 내용만 바꾸면 됩니다
- `sitemap.xml`의 `<lastmod>` 날짜도 함께 바꿔 주면 좋아요
- LinkedIn / Scholar / ORCID 버튼은 현재 각 사이트 첫 화면으로 연결되어 있어요. 본인 프로필 주소로 바꿔 주세요 (Claude에게 주소를 알려주면 반영해 드립니다)
