# ⚡ Table of Contents

1. [Decoration](#decoration)
2. [Shortcut Keys](#shortcut-keys)
3. [MarkDown Uses](#markdown-uses)
4. [GitHub <--> vsCode](#git-vscode)
5. [Commit & Push](#commitpush)

---

## Decoration <a name="decoration"></a>

- **[Awesome Badges](https://github.com/badges/awesome-badges)**
  - Various Icons & Badges

- [Simple Badge](https://badges.pages.dev/)

- [Simple Icon](simpleicons.org/)
  - 사용법
  `<img src="https://img.shields.io/badge/기술이름-#제외색상번호?style=for-the-badge&logo=아이콘이름&logoColor=white">`
  - 출처 : https://byul191oh.tistory.com/214

- 

---

## Shortcut Keys <a name="shortcut-keys"></a>

### GitHub Shortcuts
- Ctrl + 0 : 확대/축소를 기본 텍스트 크기로 다시 설정
- Ctrl + = : 더 큰 텍스트 및 그래픽을 위해 확대
- Ctrl + - : 더 작은 텍스트 및 그래픽을 위해 축소
- Ctrl + P : GitHub에 최신 커밋 푸시
- Ctrl + Shift + G : GitHub에서 리포지토리 보기
- 
  
### MarkDown Shortcuts
- Ctrl + b : 글씨체를 굵게 (bold)
- Ctrl + i : 글씨체를 기울여줌 (italic)
- Window + . : 이모지나 수학 기호 등
- 

---

## MarkDown Uses <a name="markdown-uses"></a>

---

## GitHub <--> vsCode <a name="git-vscode"></a>

### 1. GitHub 계정과 Repository 설정

먼저 GitHub에 계정을 가지고 있어야 하며, 작업하고자 하는 프로젝트를 GitHub에 Repository로 생성합니다.

### 2. vscode와 GitHub 연동

#### 2.1. vscode에서 GitHub Extension 설치

vscode의 Extension Marketplace에서 GitHub Extension for Visual Studio Code를 설치합니다. 이 Extension을 통해 GitHub와의 연동을 간편하게 설정할 수 있습니다.

#### 2.2. GitHub 계정 연동

vscode의 왼쪽 사이드바에서 Source Control 아이콘(거미줄 모양)을 클릭하고, 하단의 "No source control providers active" 메시지를 클릭하여 GitHub을 선택하고 로그인합니다. 이 과정을 통해 GitHub 계정을 vscode에 연결합니다.

#### 2.3. GitHub Repository Clone

GitHub에서 복제(clone)하고자 하는 Repository를 선택하고, "Clone Repository"를 클릭하여 로컬로 복제합니다. 이를 통해 로컬 환경에 GitHub Repository를 가져옵니다.

### 3. 파일 수정 및 Commit & Push

#### 3.1. 파일 수정

vscode에서 파일을 수정하고 저장합니다. 이 때, 수정한 파일은 로컬에서 변경이 이루어집니다.

#### 3.2. Commit

파일을 수정하고 저장한 후, vscode의 Source Control 패널에서 수정된 파일을 선택하고 Commit 메시지를 작성하여 Commit을 수행합니다. 이 과정에서 로컬 저장소에 변경 내용이 저장됩니다.

#### 3.3. Push

Commit을 했으면, vscode의 하단에 "Push" 버튼을 클릭하여 GitHub에 변경 사항을 Push합니다. 이렇게 하면 GitHub 원격 저장소에 최신 변경 내용이 업로드됩니다.

### 4. 다른 환경에서 작업할 때

집에 가거나 다른 장소에서 작업할 때는 GitHub 원격 저장소에서 최신 코드를 가져와(vscode의 Pull 기능을 사용) 작업을 진행하면 됩니다. 이후 다시 Commit & Push하여 변경 사항을 GitHub에 업데이트할 수 있습니다.

### 요약

vscode와 GitHub를 연동하여 파일을 관리하면 로컬 환경에서의 작업과 GitHub 원격 저장소 간의 실시간 동기화가 가능해집니다. 이를 통해 파일을 매번 수동으로 옮기는 번거로움을 줄이고, 작업 내용을 보다 체계적으로 관리할 수 있습니다.

---

## Commit과 Push란 <a name="commitpush"></a>

`Push`는 Git에서 사용되는 용어로, 로컬 저장소에 저장된 Commit 기록들을 원격 저장소(일반적으로 GitHub, GitLab, Bitbucket 등)에 업로드하는 작업을 말합니다. 즉, 로컬 저장소에서 수행한 변경 사항들을 원격 저장소에 동기화하는 과정입니다.

### 주요 개념과 동작:

1. **Commit**: 로컬 저장소에 있는 변경 내용을 기록하는 작업입니다. `Commit`을 하면 현재 변경된 파일들이 로컬 저장소의 히스토리에 저장됩니다.

2. **Push**: 로컬 저장소에 저장된 Commit들을 원격 저장소로 전송하는 작업입니다. `Push`를 하면 로컬 저장소에 있는 Commit들이 원격 저장소에 업로드되어 다른 사람들과 공유할 수 있습니다.

### 주요 사용 시나리오:

- **협업**: 여러 사람이 같은 프로젝트를 작업할 때, 각자가 수정한 내용을 Commit 후에 Push하여 원격 저장소에 업데이트합니다. 이를 통해 팀원들이 최신 코드를 공유하고 협력할 수 있습니다.

- **백업**: 로컬 저장소에만 있는 코드 변경 사항을 원격 저장소에 백업하여 데이터 손실을 방지합니다.

- **CI/CD (Continuous Integration / Continuous Deployment)**: 소프트웨어 개발 과정에서 자동화된 빌드, 테스트, 배포 작업을 관리할 때 `Push`를 사용하여 자동화된 배포 파이프라인을 작동시킵니다.

### Push 과정:

1. **로컬 저장소 Commit**: `git commit` 명령을 사용하여 로컬 저장소에 변경 사항을 Commit 합니다.

2. **원격 저장소 Push**: `git push` 명령을 사용하여 Commit된 변경 사항을 원격 저장소로 업로드합니다. 예를 들어,

   ```bash
   git push origin main
   ```

   위 명령은 `main` 브랜치에 Commit된 변경 사항을 원격 저장소인 `origin`에 Push하는 예시입니다.

### Push의 중요성:

`Push`를 통해 로컬에서 작업한 변경 사항들을 원격 저장소에 공유할 수 있습니다. 이를 통해 프로젝트의 투명성을 유지하고, 협업과 개발 과정의 효율성을 높일 수 있습니다.
