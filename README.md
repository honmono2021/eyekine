# EYEKINE - 안검운동학과 눈재수술

eyekine.com 웹사이트 소스코드

## 폴더 구조

```
/
├── index.html              # 메인 홈페이지
├── post-template.html      # 글 작성 템플릿
├── posts/                  # 개별 글들을 저장할 폴더
│   └── example-post.html
├── images/                 # 이미지 파일 저장
└── README.md
```

## 새 글 추가하는 방법

1. `post-template.html` 파일을 복사
2. `posts/` 폴더에 새 이름으로 저장 (예: `posts/revision-surgery-basics.html`)
3. 파일을 열어서 다음 부분 수정:
   - `<title>` 태그: 글 제목
   - `<meta name="description">`: 글 요약
   - `.article-category`: 카테고리명
   - `<h1>`: 글 제목
   - `.article-summary`: 글 소개
   - `.article-content`: 본문 내용

4. GitHub에 파일 업로드
5. 자동으로 사이트에 반영됨

## 이미지 추가 방법

1. `images/` 폴더에 이미지 업로드
2. 글에서 이미지 태그 추가:
   ```html
   <img src="../images/your-image.jpg" alt="이미지 설명">
   ```

## GitHub Pages 배포

1. GitHub에 새 repository 생성 (public)
2. 이 파일들을 모두 업로드
3. Settings > Pages에서 Source를 "main branch"로 설정
4. Custom domain에 `eyekine.com` 입력
5. 도메인 등록 사이트(가비아 등)에서 DNS 설정:
   - A 레코드:
     - 185.199.108.153
     - 185.199.109.153
     - 185.199.110.153
     - 185.199.111.153
   - CNAME 레코드: www → [username].github.io

## 도메인 리다이렉트 (eyelid-kinesiology.com → eyekine.com)

도메인 등록 사이트에서 URL 포워딩/리다이렉트 설정:
- eyelid-kinesiology.com → https://eyekine.com (301 영구 리다이렉트)

## 유지보수

- 글 수정: 해당 HTML 파일 수정 후 GitHub에 푸시
- 디자인 변경: 모든 파일의 `<style>` 부분 수정
- 메인 페이지 글 목록 업데이트: index.html의 posts-grid 섹션 수정
