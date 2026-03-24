# 멋쟁이사자처럼 순천향대학교 14기 - AI트랙 과제 제출 저장소

멋쟁이사자처럼 순천향대학교 14기 **AI트랙** 아기사자들의 주차별 과제를 제출하는 공간입니다.

---

## 폴더 구조

```
14th_AI_ASSIGNMENT/
├── README.md
├── 01_홍길동/
│   ├── 1주차/
│   │   └── 1주차과제_홍길동.ipynb
│   ├── 2주차/
│   │   └── 2주차과제_홍길동.ipynb
│   ├── 3주차/
│   │   └── 3주차과제_홍길동.ipynb
│   └── ...
├── 02_김철수/
│   ├── 1주차/
│   │   └── 1주차과제_김철수.ipynb
│   └── ...
├── 23_조아람/
│   ├── 1주차/
│   │   └── 1주차과제_조아람.ipynb
│   └── ...
└── ...
```

---

## 과제 제출 전체 흐름

```
원본 저장소 (LikeLionSCH)
       │
       │ ① Fork (내 계정으로 복사)
       ▼
내 Fork 저장소 (내 GitHub)
       │
       │ ② Clone (내 컴퓨터로 다운로드)
       ▼
내 컴퓨터에서 작업
  ├── 폴더 생성
  ├── 과제 파일 추가
  ├── ③ git add & commit (변경사항 기록)
  └── ④ git push (내 Fork에 업로드)
       │
       │ ⑤ Pull Request (원본 저장소에 반영 요청)
       ▼
원본 저장소에 반영 완료!
```

---

## 과제 제출 방법 (상세 가이드)

### 1단계: 저장소 Fork하기

> **Fork란?** 원본 저장소를 **내 GitHub 계정으로 통째로 복사**하는 것입니다. 내 복사본에서 자유롭게 작업할 수 있어요.

1. 이 저장소 페이지(`https://github.com/LikeLionSCH/14th_AI_ASSIGNMENT`)에 접속합니다.
2. 오른쪽 상단의 **`Fork`** 버튼을 클릭합니다.
3. **`Create fork`** 를 클릭합니다.
4. 잠시 기다리면 내 계정에 `https://github.com/{내_GitHub_ID}/14th_AI_ASSIGNMENT` 저장소가 생깁니다.

> Fork는 **최초 1회만** 하면 됩니다. 다음 주차부터는 이미 Fork된 저장소를 계속 사용해요.

---

### 2단계: 내 컴퓨터로 Clone하기

> **Clone이란?** GitHub에 있는 저장소를 **내 컴퓨터로 다운로드**하는 것입니다.

터미널(또는 Git Bash)을 열고 아래 명령어를 입력합니다:

```bash
# 내 Fork 저장소를 로컬로 가져오기
git clone https://github.com/{내_GitHub_ID}/14th_AI_ASSIGNMENT.git
```

> `{내_GitHub_ID}` 부분을 **본인의 GitHub 아이디**로 바꿔주세요!
>
> 예시: `git clone https://github.com/joaram/14th_AI_ASSIGNMENT.git`

```bash
# 다운로드된 폴더로 이동
cd 14th_AI_ASSIGNMENT
```

> Clone도 **최초 1회만** 하면 됩니다.

---

### 3단계: 본인 폴더 & 주차 폴더 생성하기

```bash
# 본인 번호_이름으로 폴더 생성 (-p 옵션: 하위 폴더까지 한번에 생성)
mkdir -p 23_조아람/1주차
```

> **폴더명 규칙**
> - 개인 폴더: `번호_이름` (예: `01_홍길동`, `15_김영희`, `23_조아람`)
> - 주차 폴더: `N주차` (예: `1주차`, `2주차`, `3주차`)

---

### 4단계: 과제 파일 넣기

만들어진 주차 폴더 안에 과제 파일을 넣어주세요.

```
23_조아람/
└── 1주차/
    └── 1주차과제_조아람.ipynb    ← 여기에 파일을 넣으면 됩니다!
```

> **파일명 규칙**: `N주차과제_이름.확장자`
>
> | 주차 | 파일명 예시 |
> |------|------------|
> | 1주차 | `1주차과제_조아람.ipynb` |
> | 2주차 | `2주차과제_조아람.ipynb` |
> | 3주차 | `3주차과제_조아람.ipynb` |

---

### 5단계: 변경사항 기록하기 (Add & Commit)

> **Add**는 "이 파일을 기록할 거야"라고 Git에게 알려주는 것이고,
> **Commit**은 변경사항을 **하나의 기록(스냅샷)으로 저장**하는 것입니다.

```bash
# 변경된 파일을 스테이징 (기록 준비)
git add .

# 커밋 메시지와 함께 기록 저장
git commit -m "1주차 과제 제출 - 조아람"
```

> **커밋 메시지 형식**: `N주차 과제 제출 - 이름`

---

### 6단계: 내 Fork 저장소에 올리기 (Push)

> **Push**는 내 컴퓨터의 기록을 **GitHub(내 Fork 저장소)에 업로드**하는 것입니다.

```bash
git push origin main
```

> 처음 Push할 때 GitHub 로그인을 요구할 수 있습니다.

---

### 7단계: Pull Request(PR) 보내기

> **Pull Request(PR)란?** 내 Fork에서 작업한 내용을 **원본 저장소에 "이거 반영해주세요"라고 요청**하는 것입니다. 운영진이 확인 후 merge(반영)해줍니다.

1. **내 Fork 저장소** (`https://github.com/{내_GitHub_ID}/14th_AI_ASSIGNMENT`)에 접속합니다.

2. 상단에 아래와 같은 메시지가 보입니다:
   ```
   This branch is 1 commit ahead of LikeLionSCH/14th_AI_ASSIGNMENT:main
   ```

3. **`Contribute`** 버튼을 클릭한 후 → **`Open pull request`** 를 클릭합니다.

4. PR 정보를 확인 & 입력합니다:
   - **base repository**: `LikeLionSCH/14th_AI_ASSIGNMENT` ← `main` (원본, 자동 설정됨)
   - **head repository**: `{내_GitHub_ID}/14th_AI_ASSIGNMENT` ← `main` (내 Fork, 자동 설정됨)
   - **제목**: `[1주차] 조아람 과제 제출`
   - **내용** (선택사항): 간단한 설명을 적어도 좋습니다.

5. **`Create pull request`** 버튼을 클릭하면 **제출 완료!**

---

## 처음 이후부터는 이렇게! (이후 주차 제출)

### 먼저: 원본 저장소와 동기화하기

다른 사람들의 과제가 merge되면 원본 저장소가 업데이트됩니다. 내 Fork가 뒤처지지 않도록 **매 주차 제출 전에 동기화**해야 합니다.

```bash
# 최초 1회: 원본 저장소를 upstream이라는 이름으로 등록
git remote add upstream https://github.com/LikeLionSCH/14th_AI_ASSIGNMENT.git

# 매번 제출 전: 원본의 최신 내용 가져오기
git fetch upstream

# 가져온 내용을 내 로컬에 합치기
git merge upstream/main

# 내 Fork 저장소에도 반영
git push origin main
```

### 그 다음: 3단계부터 반복

```bash
# 새 주차 폴더 생성
mkdir -p 23_조아람/2주차

# 과제 파일 넣기 (파일명: 2주차과제_조아람.ipynb)

# Git에 기록
git add .
git commit -m "2주차 과제 제출 - 조아람"
git push origin main

# GitHub에서 PR 생성 → 제출 완료!
```

---

## 네이밍 규칙 요약

| 항목 | 형식 | 예시 |
|------|------|------|
| **개인 폴더** | `번호_이름` | `23_조아람` |
| **주차 폴더** | `N주차` | `1주차`, `2주차`, `3주차` |
| **과제 파일명** | `N주차과제_이름.확장자` | `2주차과제_조아람.ipynb` |
| **커밋 메시지** | `N주차 과제 제출 - 이름` | `1주차 과제 제출 - 조아람` |
| **PR 제목** | `[N주차] 이름 과제 제출` | `[1주차] 조아람 과제 제출` |

---

## 자주 묻는 질문 (FAQ)

### Q. Fork는 매번 해야 하나요?

**A.** 아니요! Fork는 **최초 1회만** 하면 됩니다. 이후에는 같은 Fork 저장소에서 계속 작업하면 돼요.

### Q. PR은 꼭 해야 하나요? 그냥 Push하면 안 되나요?

**A.** Push는 내 Fork 저장소에만 올라갑니다. 원본 저장소(`LikeLionSCH`)에 반영하려면 **반드시 PR을 보내야** 합니다. PR을 통해 운영진이 과제를 확인하고 merge해줍니다.

### Q. PR을 보냈는데 충돌(Conflict)이 났어요!

**A.** 다른 사람의 변경사항과 겹치는 부분이 있을 때 발생합니다. 본인 폴더에서만 작업했다면 거의 발생하지 않지만, 만약 발생하면:

```bash
git fetch upstream
git merge upstream/main
# 충돌이 난 파일을 열어서 수동으로 해결한 후
git add .
git commit -m "충돌 해결"
git push origin main
```

그러면 PR에 자동으로 반영됩니다.

### Q. 이미 제출한 과제를 수정하고 싶어요!

**A.** PR이 아직 merge 되지 않았다면, 파일을 수정하고 다시 commit & push하면 **기존 PR에 자동 반영**됩니다.

```bash
# 파일 수정 후
git add .
git commit -m "1주차 과제 수정 - 조아람"
git push origin main
```

### Q. Git이 처음이에요. 어디서부터 시작하나요?

**A.** 아래 순서를 따라해보세요:

1. **Git 설치**: https://git-scm.com/downloads 에서 다운로드
2. **Git 초기 설정** (터미널에서 입력):
   ```bash
   git config --global user.name "조아람"
   git config --global user.email "your-email@example.com"
   ```
3. 위의 **1단계(Fork)부터** 차근차근 따라하면 됩니다!

---

## 주의사항

- **다른 사람의 폴더를 절대 수정하지 마세요.** 본인 폴더 내에서만 작업합니다.
- **파일명 규칙을 꼭 지켜주세요.** 통일된 형식으로 관리해야 합니다.
- 과제 파일 외에 불필요한 파일(`.DS_Store`, `__pycache__` 등)은 커밋하지 않도록 주의해주세요.
- **제출 기한을 꼭 지켜주세요!** PR 생성 시간 기준으로 확인합니다.

---

## .gitignore 권장 설정

프로젝트 루트에 `.gitignore` 파일을 만들어 불필요한 파일이 커밋되지 않도록 설정하세요:

```
.DS_Store
__pycache__/
*.pyc
.ipynb_checkpoints/
.env
```

---

**멋쟁이사자처럼 순천향대학교 14기 AI트랙** 화이팅! 🦁
