# 교육평가 교과목 소개 페이지

연성대학교 유아교육과 2학년 교직선택 「교육평가」(2학점) 교과목 소개 정적 웹페이지입니다.

- 담당: 김민선 교수
- 주교재: 서동기·엄재춘, 『교육평가』, 동문사
- 구성: 15주 주차별 계획 · 팀 산출물 12종 · 학습성과 CO1~CO4 · 평가 기준 · 성적 반영 비율

## 파일 구성

| 파일 | 설명 |
|---|---|
| `index.html` | 교과목 소개 페이지 본문 (CSS·JS 내장, 외부 리소스 없음) |
| `404.html` | 잘못된 주소 접근 시 안내 페이지 |
| `.nojekyll` | GitHub Pages의 Jekyll 빌드를 건너뛰게 하는 표시 파일 |

## GitHub Pages 배포 방법

### 1. GitHub에 저장소 만들기

GitHub에서 새 저장소를 만듭니다(예: `edu-evaluation`). README·.gitignore 등은 추가하지 않고 빈 저장소로 만드세요.

### 2. 이 폴더를 저장소에 올리기

아래 명령에서 `USERNAME`과 `REPO`를 본인 것으로 바꿔 실행합니다.

```bash
git init -b main
git add .
git commit -m "교육평가 교과목 소개 페이지"
git remote add origin https://github.com/USERNAME/REPO.git
git push -u origin main
```

### 3. Pages 켜기

저장소 페이지에서 **Settings → Pages → Build and deployment → Source** 를 **Deploy from a branch** 로 두고, 브랜치는 `main`, 폴더는 `/ (root)` 로 지정합니다.

1~2분 뒤 아래 주소에서 페이지가 열립니다.

```
https://USERNAME.github.io/REPO/
```

### 4. 수정 후 다시 배포하기

`index.html`을 고친 뒤 커밋·푸시하면 자동으로 다시 배포됩니다.

```bash
git add index.html
git commit -m "주차별 내용 수정"
git push
```

## 로컬에서 미리 보기

`index.html`을 브라우저로 바로 열어도 되고, 로컬 서버로 확인하려면:

```bash
python -m http.server 8000
```

브라우저에서 `http://localhost:8000` 으로 접속합니다.

## 내용 수정 가이드

주차별 계획은 `index.html` 하단 `<script>` 안의 `WEEKS` 배열에서 관리합니다. 각 항목의 필드는 다음과 같습니다.

| 필드 | 내용 |
|---|---|
| `w` | 주차 번호 |
| `tag` | `""`(일반) / `"issue"`(최신 이슈) / `"event"`(전시·갤러리 워크) — 필터 버튼과 색상을 결정 |
| `label` | 주차 배지에 표시할 문구 |
| `title` | 주차 제목 |
| `theory` | 이론 항목 배열 |
| `book` | 교재 장 표기 |
| `act` | 팀활동 설명 |
| `out` | 팀 산출물 |
| `run` | 시간 운영 배분 |

색상은 `:root`의 CSS 변수에서 한 번에 바꿀 수 있습니다.

## 남은 확인 사항

- **교재 장 매핑** — 각 주차의 "교재 ▸" 표기는 표준적인 『교육평가』 구성으로 잠정 배치한 것으로, 실제 목차와 대조해 확정이 필요합니다.
- **13·14주차 정책 사실관계** — 유보통합 추진 경과, 어린이집 평가제·유치원 평가의 현행 주기와 지표는 1차 출처(i-nuri.go.kr, moe.go.kr, kcpi.or.kr 등)로 재확인이 필요합니다.
- **학과 인재상·직무역량 연계 문구** — 확보되면 각 CO 아래에 추가할 수 있습니다.
