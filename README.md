# 제출물: Python & Git 기초 - 프롬프트 관리 프로그램

## 1. GitHub 저장소

https://github.com/dusgn0330/prompt-manager

---

## 2. 개발 환경 설정

### 2-1. VSCode에서 Python 파일 작성 및 실행

`hello.py`에 `print("Hello")`를 작성하고 터미널에서 실행했습니다.

![hello.py 실행](images/01-hello-run.png)

> 처음에는 코드 앞에 공백이 들어가 `IndentationError: unexpected indent`가 발생했고, 공백을 지운 뒤 정상 실행했습니다.

### 2-2. Python / Git 버전 확인

![버전 확인](images/02-versions.png)

- Python 3.15.2 (3.10 이상 조건 충족)
- git version 2.56.0.windows.4

### 2-3. Git 사용자 정보 및 기본 브랜치 설정

```
git config --global user.name "dusgn0330"
git config --global user.email "(이메일)"
git config --global init.defaultBranch main
git config --list
```

![git config](images/03-git-config.png)

### 2-4. VSCode GitHub 로그인

VSCode 계정 메뉴에 GitHub 계정(`dusgn0330`)이 연결된 것을 확인했습니다.

![GitHub 로그인](images/04-github-login.png)

---

## 3. 프로그램 실행 결과

실행 방법: `python prompt_manager.py`

### 3-1. 메뉴 화면과 기본 프롬프트 목록

메뉴가 출력되고, 기본 프롬프트 5개가 등록되어 있습니다.

![메뉴와 기본 목록](images/05-menu-default-list.png)

### 3-2. 프롬프트 추가

입력값이 비어 있으면 다시 입력을 요청합니다.

![빈 값 입력](images/06-add-empty-input.png)

제목, 내용, 카테고리를 입력하면 프롬프트가 추가됩니다.

![프롬프트 추가 성공](images/07-add-success.png)

### 3-3. 프롬프트 목록

기본 프롬프트 5개와 실행 중 추가한 3개, 총 8개가 표시됩니다.

![프롬프트 목록](images/08-list-8.png)

### 3-4. 카테고리별 조회

![카테고리별 조회](images/09-category.png)

### 3-5. 프롬프트 검색과 잘못된 입력 처리

키워드 검색 결과가 출력되고, 메뉴에 없는 값(`zds`)을 입력하면 안내 메시지 후 메뉴가 다시 표시됩니다.

![검색과 잘못된 입력](images/10-search-invalid-input.png)

### 3-6. 프롬프트 상세 보기

잘못된 번호(99)를 입력하면 안내 메시지가 출력됩니다.

![상세 보기](images/11-detail.png)

### 3-7. 즐겨찾기 관리 및 목록

즐겨찾기를 추가한 뒤 목록에서 ⭐와 함께 확인합니다.

![즐겨찾기](images/12-favorites.png)

---

## 4. Git 작업 기록

### 4-1. git log --oneline --graph

`feature/list` 브랜치를 만들어 목록 기능을 작업한 뒤 `main`으로 병합했습니다. 커밋은 총 13개입니다.

![git log graph](images/13-git-log-graph.png)

### 4-2. 첫 푸시

![첫 푸시](images/14-first-push.png)

### 4-3. 사용한 Git 명령어

| 명령어 | 사용한 곳 |
|---|---|
| init | 프로젝트 폴더에서 로컬 저장소 시작 |
| add / commit | 기능 단위로 커밋 (총 13개) |
| push | 원격 저장소(GitHub)에 업로드 |
| clone | 공개 샘플 저장소를 내려받아 구조와 로그 확인 |
| checkout | `feature/list` 브랜치 생성 및 `main` 복귀 |
| merge | `feature/list`를 `main`에 병합 (`--no-ff`) |
| pull | GitHub 웹에서 수정한 README를 로컬로 가져옴 |

---

## 5. 기본 프롬프트 데이터

이전 미션(자동화 프로젝트 1, 2)을 바탕으로 정리한 프롬프트 5개를 기본 데이터로 등록했습니다.

| 제목 | 카테고리 |
|---|---|
| 자동화 워크플로우 설계 도우미 | 자동화 |
| 기상청 API 데이터 가공 도우미 | 자동화 |
| 자동화 도구 비교 보고서 | 텍스트 생성 |
| 우산 알림 메일 문구 작성 | 텍스트 생성 |
| 노코드 자동화 멘토 | 페르소나 |

---

## 6. 요구사항 체크리스트

- [x] 콘솔 메뉴 기반 프로그램 (추가, 목록, 카테고리별 조회, 검색, 상세 보기, 즐겨찾기)
- [x] 리스트와 딕셔너리로 데이터 저장, 기본 프롬프트 3개 이상 (5개)
- [x] 기능별 함수 분리, 외부 라이브러리 미사용
- [x] GitHub 저장소 업로드
- [x] 의미 있는 커밋 10개 이상 (13개)
- [x] 브랜치 생성 및 병합 기록
- [x] init, add, commit, push, pull, checkout, clone, merge 각 1회 이상 사용
- [x] README.md 작성 (프로그램 설명, 실행 방법, 기능 목록, 카테고리 설명)
