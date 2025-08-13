---
title: 블로그 포스트 작성법
date: 2025-01-13 15:30:00 +0900
categories: [Tutorial, Blogging]
tags: [jekyll, chirpy, markdown]
author: KnowledgeLupin
toc: true
comments: false
math: true
mermaid: true
---

## 머리말 (Front Matter)
모든 포스트는 `---`로 감싸진 머리말이 필요합니다.

### 필수 항목
- `title`: 포스트 제목
- `date`: 작성 날짜 (YYYY-MM-DD HH:MM:SS +0900)
- `categories`: [대분류, 소분류] 형식
- `tags`: [태그1, 태그2, ...] 형식

### 선택 항목
- `author`: 작성자 (기본값은 _config.yml의 설정)
- `toc`: 목차 표시 여부 (true/false)
- `comments`: 댓글 허용 여부
- `math`: 수식 사용 여부
- `mermaid`: 다이어그램 사용 여부
- `pin`: 상단 고정 여부
- `image`: 대표 이미지 설정

## 마크다운 문법 예시

### 텍스트 스타일
- **굵은 글씨**: `**텍스트**` → **텍스트**
- *기울임*: `*텍스트*` → *텍스트*
- ~~취소선~~: `~~텍스트~~` → ~~텍스트~~
- `인라인 코드`: `` `코드` ``

### 링크와 이미지
```markdown
[링크 텍스트](https://url.com)
![이미지 설명](/path/to/image.jpg)
```

### 코드 블록
```python
def hello_world():
    print("Hello, World!")
    return True
```

### 수식 (math: true 필요)
인라인 수식: $a^2 + b^2 = c^2$

블록 수식:
$$
\int_{-\infty}^{\infty} e^{-x^2} dx = \sqrt{\pi}
$$

### 테이블
| 헤더1 | 헤더2 | 헤더3 |
|:------|:-----:|------:|
| 왼쪽정렬 | 중앙정렬 | 오른쪽정렬 |
| 데이터1 | 데이터2 | 데이터3 |

### 인용문
> 이것은 인용문입니다.
> 여러 줄로 작성 가능합니다.

### 목록
1. 순서 있는 목록
2. 두 번째 항목
   - 중첩 가능
   - 하위 항목

- 순서 없는 목록
- 두 번째 항목
  1. 중첩 가능
  2. 번호 목록도 가능

### 작업 목록
- [x] 완료된 작업
- [ ] 미완료 작업

### 알림 박스 (Chirpy 테마 특별 기능)
> 일반 정보입니다.
{: .prompt-info }

> 팁입니다.
{: .prompt-tip }

> 경고입니다.
{: .prompt-warning }

> 위험입니다.
{: .prompt-danger }

## 파일 경로 예시
```
_posts/
├── 2025-01-13-welcome.md
├── 2025-01-13-how-to-write-post.md
└── 2025-01-14-next-post.md
```

## 이미지 추가
1. `/assets/img/` 폴더에 이미지 저장
2. 포스트에서 참조:
```markdown
![설명](/assets/img/my-image.png)
```

## 포스트 발행
1. 파일 저장
2. Git 커밋 & 푸시
3. GitHub Actions가 자동 빌드
4. 몇 분 후 블로그에 게시됨