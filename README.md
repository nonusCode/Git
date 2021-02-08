# Git



### 저장소 설정

> `.git`이라는 숨김폴더 생성
>
> `git bash`에서 `(master)`라는 branch 생성

```bash
$ git init
```



### 초기 설정(계정 연동)

```bash
# 전역 설정
$ git config --global user.email "GitHub@email"
$ git config --global user.name "GitHub@name"

# 지역 설정
$ git config --local user.email "GitHub@email"
$ git config --local user.name "GitHub@name"
```



### 원격저장소 설정(리포지터리 연동)

```bash
$ git remote add origin https://github.com/~
```



### add

> `git`에서 `commit`할 대상을 `staging area`로 이동시키는 명령어

```bash
# 모든 파일 및 폴더를 stage
$ git add .

# 특정 파일, 폴더를 stage
$ git add nonus/README.md
```



### commit

> `git`에 이력을 남기기 위한 명령어

```bash
$ git commit -m "Message"
```



### push

> 원격저장소에 업로드를 위한 명령어

```bash
$ git push origin master
```



### 가상환경 설정(git bash)

> Python 3.5.3 (Current)
>
> Python 3.7.3 (New)

1. 시스템 환경 변수 => 환경 변수 => 사용자 변수 => Path 선택 후 편집 `~\Python37\Scripts\`,  `~\Python37\` 유무 확인

2. 시스템 환경 변수 => 환경 변수 => 시스템 변수 => Path 선택 후 편집 `~\Python35\Scripts\`,  `~\Python35\` 제거

   > Path가 잡혀있지 않다면, Install된 경로 찾아서 넣어줘야 함

3. Python 가상환경 생성 및 실행

   ```bash
   # 버전 확인
   $ python -V
   Python 3.7.3
   # 가상환경 폴더 생성
   $ mkdir ~/PythonVirtualenv
   # 새로운 버전의 이름으로 가상환경 생성
   $ python -m venv ~/PythonVirtualenv/3.7.3
   # 가상환경 실행
   $ source ~/PythonVirtualenv/3.7.3/Scripts/activate
   # 정상 실행 시 아래와 같이 가상환경 이름이 표시됨
   (python-3.7.3)
   # 가상환경 종료
   $ deactivate
   # 버전 확인
   $ python -V
   Python 3.5.3
   ```

4. 시스템 환경 변수 => 환경 변수 => 시스템 변수 => Path 선택 후 편집 `~\Python35\Scripts\`,  `~\Python35\` 추가

5. .bash_prifile 유무 확인 및 생성

   ```bash
   # 숨겨진 폴더나 파일을 포함한 모든 폴더의 자세한 내용을 보여줌
   $ ls -al
   # .bash_prifle이 없는 경우 생성
   $ touch .bash_prifle
   # 확인
   $ ls -al
   ```

6. .bash_profile 파일 편집

   ```bash
   # vi 편집기 실행
   $ vi .bash_profile
   # 입력 모드로 전환
   i
   # 가상환경 실행 명령어 입력
   source ~/PythonVirtualenv/3.7.3/Scripts/activate
   # 저장
   ESC를 눌러 명령모드로 전환 후 :wq를 입력
   ```

7. .bashrc 생성 및 .bashrc 파일 편집

   ```bash
   # .bashrc 생성
   $ touch .bashrc
   # vi 편집기 실행
   $ vi .bashrc
   # 가상환경 실행 명령어 입력
   source ~/PythonVirtualenv/3.7.3/Scripts/activate
   # 저장
   ESC를 눌러 명령모드로 전환 후 :wq를 입력
   ```