# AXIS Design Gallery

BI MATRIX의 디자인 레퍼런스 갤러리 사이트입니다. 산업군·화면 유형·활용 목적별로 분류된 대시보드/리포팅 디자인 레퍼런스와 디자인 리소스(차트, 컬러, 폰트 등)를 제공합니다.

**Live**: https://back2zion.github.io/design_gallery/

## 페이지 구성

| 페이지 | 파일 | 설명 |
|---|---|---|
| 메인 | `index.html` | 히어로, 추천 레퍼런스, 디자인 리소스 미리보기 |
| 레퍼런스 갤러리 | `gallery.html` | 산업군/화면유형/목적/레이아웃/디자인톤 필터 및 검색 |
| 디자인 리소스 | `resources.html` | 차트, 컬러 팔레트, 폰트 등 디자인 리소스 |
| 고객사 사이트 | `archive.html` | 고객사 프로젝트 아카이브 |

## 기술 스택

- React 18 (UMD) + Babel Standalone — 빌드 과정 없이 HTML 안에 JSX를 인라인으로 작성
- Tailwind CSS (CDN) + `styles.css` 커스텀 스타일
- 정적 사이트 — 별도 서버/빌드 불필요

## 주요 기능

- **검색**: 모든 페이지 상단 헤더 검색창에서 Enter 입력 시 `gallery.html?q=검색어`로 이동해 레퍼런스 갤러리를 필터링
- **필터**: 갤러리 페이지에서 산업군, 화면 유형, 활용 목적, 레이아웃 구조, 디자인톤 다중 필터
- **다크/라이트 테마**: `localStorage`(`axis-theme`)에 저장
- **다국어**: 한국어/영어/일본어 — 헤더의 언어 버튼으로 전환, `localStorage`(`axis-lang`)에 저장

## 로컬 실행

빌드가 필요 없습니다. 정적 서버로 열면 됩니다.

```bash
npx serve .
# 또는
python3 -m http.server 8000
```

## 배포

`main` 브랜치에 푸시하면 GitHub Actions(`.github/workflows/pages.yml`)가 GitHub Pages로 자동 배포합니다.

## 디렉터리 구조

```
├── index.html              # 메인 페이지
├── gallery.html            # 레퍼런스 갤러리
├── resources.html          # 디자인 리소스
├── archive.html            # 고객사 사이트(프로젝트 아카이브)
├── styles.css              # 공통 스타일
├── images/
│   ├── templates/          # 레퍼런스 원본 이미지
│   ├── templates-thumbnail/# 레퍼런스 썸네일
│   ├── archive/            # 아카이브 이미지
│   ├── logos/              # 고객사 로고
│   └── fonts/              # 폰트 미리보기 이미지
└── .github/workflows/      # GitHub Pages 배포 워크플로우
```

---

© BI MATRIX CO., LTD. ALL RIGHTS RESERVED.
