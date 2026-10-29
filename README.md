# 제출물: Python & Git 기초 - 프롬프트 관리 프로그램

## 1. GitHub 저장소

https://github.com/dusgn0330/prompt-manager

---

## 2. 개발 환경 설정

### 2-1. VSCode에서 Python 파일 작성 및 실행

`hello.py`에 `print("Hello")`를 작성하고 터미널에서 실행했습니다.

![hello.py 실행](images/01-hello-run.png)

```
PS C:\Users\dusgn\prompt-manager> python hello.py
Hello
```

> 처음에는 코드 앞에 공백이 들어가 `IndentationError: unexpected indent`가 발생했고, 공백을 지운 뒤 정상 실행했습니다.

### 2-2. Python / Git 버전 확인

![버전 확인](images/02-versions.png)

```
python --version
git --version
```

### 2-3. Git 사용자 정보 및 기본 브랜치 설정

```
git config --global user.name "dusgn0330"
git config --global user.email "(이메일)"
git config --global init.defaultBranch main
git config --list
```

![git config](images/03-git-config.png)

```
user.name=dusgn0330
user.email=(이메일)
init.defaultbranch=main
```

### 2-4. VSCode GitHub 로그인

VSCode 계정 메뉴에 GitHub 계정(`dusgn0330`)이 연결된 것을 확인했습니다.

![GitHub 로그인](images/04-github-login.png)

---

## 3. 프로그램 실행 결과

실행 방법: `python prompt_manager.py`

### 3-1. 메뉴 화면

![메뉴](images/05-menu.png)

```
=== 나만의 프롬프트 관리 ===
1. 프롬프트 추가
2. 프롬프트 목록
3. 카테고리별 조회
4. 프롬프트 검색
5. 프롬프트 상세 보기
6. 즐겨찾기 관리
7. 즐겨찾기 목록
0. 종료
선택:
```

### 3-2. 잘못된 번호 입력

```
선택: zds
잘못된 입력입니다. 0~7 사이의 번호를 입력해주세요.
```

![잘못된 입력](images/06-invalid-input.png)

### 3-3. 프롬프트 추가 (빈 값 입력 시 재입력 요청)

![프롬프트 추가](images/07-add-prompt.png)

```
=== 프롬프트 추가 ===
제목:
값이 비어 있습니다. 다시 입력해주세요.
제목:
```

### 3-4. 프롬프트 목록

기본 프롬프트 5개와 실행 중 추가한 3개, 총 8개가 표시됩니다.

![프롬프트 목록](images/08-list.png)

```
=== 프롬프트 목록 ===
1. [자동화] 자동화 워크플로우 설계 도우미
2. [자동화] 기상청 API 데이터 가공 도우미
3. [텍스트 생성] 자동화 도구 비교 보고서
4. [텍스트 생성] 우산 알림 메일 문구 작성
5. [페르소나] 노코드 자동화 멘토
6. [텍스트 생성] 납기일 변경 안내 메일 작성
7. [페르소나] 정중원 B2B 메일 어시스턴트
8. [자동화] 누락 정보 확인 질문 규칙
총 8개의 프롬프트
```

### 3-5. 프롬프트 검색

![프롬프트 검색](images/09-search.png)

```
=== 프롬프트 검색 ===
검색어: 메일
검색 결과:
1. [텍스트 생성] 우산 알림 메일 문구 작성
1개의 프롬프트를 찾았습니다.
```

### 3-6. 프롬프트 상세 보기

![상세 보기](images/10-detail.png)

```
=== 프롬프트 상세 보기 ===
번호 입력: 1
────────────────────────────
제목: 자동화 워크플로우 설계 도우미
카테고리: 자동화
즐겨찾기: -
────────────────────────────
내용:
당신은 Make와 Zapier에 능숙한 노코드 자동화 전문가입니다.
제가 반복하는 업무를 설명하면 Trigger, Action, 조건 분기로 나눠 워크플로우를 설계해주세요.
각 단계에서 사용할 모듈 이름과 예상되는 오류, 그리고 오류 처리 방법도 함께 알려주세요.
────────────────────────────
```

잘못된 번호 입력 시:

```
번호 입력: 99
잘못된 번호입니다. 1~5 사이의 번호를 입력해주세요.
```

### 3-7. 즐겨찾기 관리 및 목록

즐겨찾기가 없을 때 목록을 조회하면 안내 메시지가 나오고, 추가한 뒤에는 ⭐와 함께 표시됩니다.

![즐겨찾기](images/11-favorites.png)

```
=== 즐겨찾기 목록 ===
즐겨찾기한 프롬프트가 없습니다.

=== 즐겨찾기 관리 ===
프롬프트 번호 입력: 1
'자동화 워크플로우 설계 도우미' 프롬프트를 즐겨찾기에 추가했습니다!

=== 즐겨찾기 관리 ===
프롬프트 번호 입력: 3
'자동화 도구 비교 보고서' 프롬프트를 즐겨찾기에 추가했습니다!

=== 즐겨찾기 목록 ===
1. [자동화] 자동화 워크플로우 설계 도우미 ⭐
2. [텍스트 생성] 자동화 도구 비교 보고서 ⭐
총 2개의 즐겨찾기
```

---

## 4. Git 작업 기록

### 4-1. git log --oneline --graph

`feature/list` 브랜치를 만들어 목록 기능을 작업한 뒤 `main`으로 병합했습니다.

![git log graph](images/12-git-log-graph.png)

```
* 6251ef5 (HEAD -> main, origin/main, origin/HEAD) docs: README에 제작자 추가
* a42faa9 docs: README 작성
* a1ad051 feat: 즐겨찾기 관리 및 목록 기능
* 58a9c6d feat: 프롬프트 상세 보기 기능
* 6b3e016 feat: 키워드 검색 기능
* e9fa5fa feat: 카테고리별 조회 기능
* 3bca239 feat: 프롬프트 추가 기능
*   55a30a0 merge: feature/list 브랜치 병합
|\
| * daa406e (feature/list) feat: 프롬프트 목록 기능
* | 0c80587 docs: README에 실행 방법 추가
|/
* 8a05024 feat: 메뉴와 메인 루프 구현
* fbaa710 feat: 기본 프롬프트 데이터 추가
* c2b7225 chore: README, .gitignore 초기 생성
```

### 4-2. 사용한 Git 명령어

| 명령어 | 사용한 곳 |
|---|---|
| init | 프로젝트 폴더에서 로컬 저장소 시작 |
| add / commit | 기능 단위로 커밋 (총 13개) |
| push | 원격 저장소(GitHub)에 업로드 |
| clone | 공개 샘플 저장소를 내려받아 구조와 로그 확인 |
| checkout | `feature/list` 브랜치 생성 및 `main` 복귀 |
| merge | `feature/list`를 `main`에 병합 (`--no-ff`) |
| pull | GitHub 웹에서 수정한 README를 로컬로 가져옴 |

### 4-3. 첫 푸시

```
git branch -M main
git remote add origin https://github.com/dusgn0330/prompt-manager.git
git push -u origin main
```

![첫 푸시](images/13-first-push.png)

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
