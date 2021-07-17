# GIT (생활코딩)

## original git 설치

- git-csc.com
  - window 설치



## 1. 버전관리 시작

1. `mkdir [파일명]`: 파일 생성
2. `ls -al`: 파일 내부 확인
3. `git init .`:현재 디렉토리를 깃에게 버전관리하도록 명령
4. `. git` :**삭제 시** git  **전부**가 삭제



## 2. 버전단계

- `Working tree`
  - 파일 생성, 수정 하는 장소
  - 버전 생성 전 단계
- `Staging Area`
  - 버전으로 만들려고 하는 파일을 올려두는 단계
- `Repasitory (저장소) ` 
  -  버전이 저장 되어있는 장소
  -  `. git` 과 동일



## 3.1 버전의 생성

1. `nano [파일명].txt`: 파일 생성
2. `cat [파일명]`: 뒤의 파일을 내용을 출력
3. `git status`: git에게 상태를 물음
4. `git add [파일명]`: staging Area에 보내
5. `git commit -m "[제목]"`: Repasitory로 보내
6. `git log` : 히스토리 확인



## 3.2 버전의 생성 (여러 개의 파일을 하나로)

- `untracked files`: 백업 되지 않는 파일 (working tree에 위치)
- `git log --stat`: 파일의 관계를 보여줌



## 4. 버전간의 차이점 비교

- `git diff(diference)`: 차이점을 보여줌
- `git rset --hard`: repository에 올리기 전까지의 파일을 삭제
- `cat [파일명]`: 과거의 버전으로 돌아감
- `git log -p`: 변화의 히스토리를 보여줌 **추적**에 유용



## 5. checkout 과 시간여행

- `git checkout[버전 아이디]`: 해당 버전으로 돌아감
- `git checkout master`: 최신 버전으로 돌아감



## 6. 보충

- `git add .`: 현재있는 dir 모두를 추가
- `git commit -am "제목"`
  -  추가와 버전 저장을 한번에
  -  단, 한 번이라도 add가 된 이후부터 가능
- `git commit` : 여러 줄의 커밋 제목을 할 때 편리함
- `git config -- global core. editer "에디터명"`: 원하는 에디터로 바꿈



## 7. 버전 삭제 (git reset)

- `git reset --hard [버전 아이디] `: 버전 리셋
  - [] 버전을 리셋하겠다 **X**
  - [] 버전으로 리셋하겠다 **O**



## 8. 버전 복구 (git revert)

- 삭제와 보전의 목적이 달성 가능
- revert 는 최신 단계의 커밋이 필요
- 기존 버전도 존재하고 되돌린 버전으로도 변경
- `1단계` **역순**으로만 revert



## 9. TIP

- `diff tool`: 검색 엔진을 통해 다양한 tool 활용

- `.gitignore[파일명]`: 무시하고 싶은 파일을 넣어두기

- `branch`: 하나의 저장소에서 여러 개의 작업을 수행 가능 

- `tag`: 새로운 이름을 부여 (복잡한 이름 대신)

- `backup`: **필수**

  