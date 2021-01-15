# Git



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