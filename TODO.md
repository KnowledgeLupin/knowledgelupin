# GitHub 블로그 TODO List

## 📝 할 일 목록

### 댓글 기능 구현 (Giscus)
- [ ] Giscus 설정 완료하기
  - [ ] https://giscus.app 에서 설정값 생성
  - [ ] repo-id와 category-id 값 획득
  - [ ] _config.yml 파일 수정
- [ ] 댓글 기능 테스트

#### Giscus 설정 방법
1. https://giscus.app 접속
2. Repository: `knowledgelupin/knowledgelupin.github.io` 입력
3. Discussion 매핑: pathname 선택
4. Category: Announcements 선택
5. 생성된 script에서 다음 값 복사:
   - `data-repo-id`
   - `data-category-id`

#### _config.yml 수정 예시
```yaml
comments:
  provider: giscus
  giscus:
    repo: knowledgelupin/knowledgelupin.github.io
    repo_id: # 여기에 repo-id 입력
    category: Announcements
    category_id: # 여기에 category-id 입력
    mapping: pathname
    strict: 0
    input_position: bottom
    lang: ko
    reactions_enabled: 1
```

### 기타 개선사항
- [ ] 프로필 이미지 추가
- [ ] About 페이지 내용 작성
- [ ] 카테고리 구조 정리
- [ ] 태그 시스템 구축
- [ ] SEO 최적화
- [ ] Google Analytics 설정
- [ ] 검색 기능 최적화

### 완료된 작업 ✅
- [x] GitHub 블로그 초기 설정
- [x] Chirpy 테마 설치
- [x] SSH 키 설정 및 계정 분리
- [x] 비공개 이메일 설정
- [x] Threads 링크 추가
- [x] 첫 포스트 작성