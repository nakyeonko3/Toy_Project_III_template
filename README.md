# Toy_Project_III_template

토이프로젝트 템플릿

## 목차

- [Toy\_Project\_III\_template](#toy_project_iii_template)
  - [목차](#목차)
  - [이 템플릿이 포함한 기능과 문서 목록](#이-템플릿이-포함한-기능과-문서-목록)
  - [사용 방법](#사용-방법)
    - [commit message 컨벤션 세팅 및 사용 방법](#commit-message-컨벤션-세팅-및-사용-방법)
    - [PR 컨벤션 세팅 및 사용 방법](#pr-컨벤션-세팅-및-사용-방법)

## 이 템플릿이 포함한 기능과 문서 목록

- issue 컨벤션
- commit message 컨벤션
- pr 컨벤션
- .gitignore
- .prettierignore
- ai 코드 리뷰
- [리드미 템플릿 READM.md](./document/README.md)
- [Git 실수 해결 백서 OhShitGit](./document/OhShitGit.md)

## 사용 방법

### commit message 컨벤션 세팅 및 사용 방법

1. pull requests 익스텐션 설치
   [github pull requests 익스텐션 링크](https://marketplace.visualstudio.com/items?itemName=GitHub.vscode-pull-request-github)

2. 해당 명령어를 프로젝트 루트 위치의 터미널창에서 입력

아래 명령어를 입력하면 커밋 템플릿 설정은 완료됨.

```bash
cd <프로젝트 위치>
git config commit.template ./.github/.gitmessage.txt
```

커밋 메시지를 적을 때 vim이 불편하다면 아래의 명령어를 입력

```bash
git config --global core.editor "code --wait"
```

3. commit message 컨벤션으로 커밋 해보기

vscode에서 커밋 버튼을 누르거나, `git commit` 명령어를 터미널에 입력

```bash
git commit
```

4. 커밋 컨벤션 템플릿 사용법 예시

```
fix: cors에 배포 도메인 koyeb.com을 추가함.
- cors 이슈로 인해 GET api/v1/employees 가 작동 안하는 문제 해결
- server/index.js 코드에 cors를 추가함.
Gihub issue: #1
```

- [커밋 컨벤션 템플릿](./.github/.gitmessage.txt)

```bash
# --- COMMIT END ---
#   <타입> 리스트
#   feat        : 기능 (새로운 기능)
#   fix         : 버그 (버그 수정)
#   refactor    : 리팩토링
#   design      : CSS 등 사용자 UI 디자인 변경
#   style       : 코드 스타일 (코드 형식, 줄바꿈, 주석, 세미콜론 추가: 비즈니스 로직에 변경 없음)
#   docs        : 문서 수정 (문서 추가, 수정, 삭제, README)
#   test        : 테스트 (테스트 코드 추가, 수정, 삭제: 비즈니스 로직에 변경 없음)
#   chore       : 기타 변경사항 (빌드 스크립트 수정, assets, package.json 변경 등)
#   init        : 초기 생성
#   rename      : 파일 혹은 폴더명을 수정하거나 옮기는 작업만 한 경우
#   remove      : 파일을 삭제하는 작업만 수행한 경우
# ------------------
#   제목 첫 글자를 대문자로
#   제목은 명령문으로
#   제목 끝에 마침표(.) 금지
#   제목과 본문을 한 줄 띄워 분리하기
#   본문은 "어떻게" 보다 "무엇을", "왜"를 설명한다.
#   본문에 여러줄의 메시지를 작성할 땐 "-"로 구분
# ------------------
#   <꼬리말>
#   필수가 아닌 optioanl
#   Fixes        :이슈 수정중 (아직 해결되지 않은 경우)
#   Resolves     : 이슈 해결했을 때 사용
#   Ref          : 참고할 이슈가 있을 때 사용
#   Related to   : 해당 커밋에 관련된 이슈번호 (아직 해결되지 않은 경우)
#   ex) Fixes: #47 Related to: #32, #21
```

### PR 컨벤션 세팅 및 사용 방법
