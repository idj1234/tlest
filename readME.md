* GitHub 원격저장소(repository)에 프로젝트 새로 올리기
1. Github 계정에 new repository 생성
   -> repository 주소 복사해두기
2. 로컬에 있는 프로젝트 폴더에 마우스 오른쪽 버튼 클릭 - Git Bash Here 선택
3. git init 
   -> default branch로 master라는 branch가 생성된다.
4. git add . 
   -> 로컬 저장소의 모든파일 git에 올리기
5. git commit -m "커밋 내용"
   -> 첫번째 올릴 때는 커밋 내용에 보통 'first commit' 이라고 씀
6. git remote add (별칭) (원격저장소(repository)주소) 
   -> 프로젝트를 올릴 repository 지정 
   -> 별칭 : 보통 처음엔 origin 으로 설정
7. git push (원격저장소 별칭) (원격 branch명) 
   -> 원격저장소 별칭 : 처음엔 origin
   -> 원격 branch명 : 처음엔 master
8. GitHub 이메일 주소 및 비밀번호 입력하여 로그인 -> 완료

* GitHub 원격저장소(repository)에서 새로운 로컬저장소로 프로젝트 끌어오기
1. 로컬에 프로젝트를 저장할 새폴더 생성하기- 마우스 오른쪽 버튼 클릭 - Git Bash Here 선택
2. git init
3. git remote add (별칭) (원격저장소 주소)
4. git remote
  -> 연결된 저장소 별칭이 뜨는지 확인
5. git pull (원격저장소 별칭) (원격 branch명)

* GitHub 원격저장소(repository)에서 작업중이던 로컬저장소로 프로젝트 끌어오기
1. 작업중인 로컬 프로젝트 - 마우스 오른쪽 버튼 클릭 - Git Bash Here 선택
2. git remote 
   -> 연결되어있는 원격저장소 별칭 및 branch명 확인 
   (이미 원격저장소와 연결되어 있는 로컬 저장소가 있다면 3번, 없다면 2-1번)
  2-1. git remote add (별칭) (원격저장소 주소)
3. git pull (원격저장소 별칭) (원격 branch명)
   -> 이때 remote로 확인했던 branch에 이어서 작업을 하려면, 해당 branch명 사용
   -> 또는, 다른 branch명을 사용해서 새로운 branch를 생성

* GitHub 기존 원격저장소(repository)에 작업중인 로컬 프로젝트 commit 하기
1. 로컬에 있는 프로젝트 폴더에 마우스 오른쪽 버튼 클릭 - Git Bash Here 선택
2. git add . 
   -> 로컬 저장소의 모든파일 git에 올리기
3. git commit -m "커밋 내용"
4. git remote 
   -> 연결되어있는 원격저장소 별칭 및 branch명 확인 
   (이미 원격저장소와 연결되어 있는 로컬 저장소가 있다면 3번, 없다면 2-1번)
  2-1. git remote add (별칭) (원격저장소 주소)
5. git push (원격저장소 별칭) (원격 branch명) 
   -> 이때 remote로 확인했던 branch에 이어서 작업을 하려면, 해당 branch명 사용
   -> 또는, 다른 branch명을 사용해서 새로운 branch를 생성

* remote 명령어
git remote show (원격저장소 이름)
 -> 원격 저장소의 세부정보 확인 가능
git remote -v
-> 현재 git 프로젝트 저장소 및 url 출력 

* error 또는 warning 해결 방법
※ LF warning 이 뜬다면 git config core.autocrlf true 명령어 입력 후 다시 git add . 명령어 입력
    -> 관련 글 참고 https://blog.sapzape.com/923
    
* fatal : unable to auto-detect email address 에러 해결
  -> git config --global user.email "you@example.com" ex)"pskdy8414@naver.com" -> gitHub ID : 이메일
     git config --global user.name "Your Name"   ex)"Delilah1004" -> gitHub 이름

* git remote add origin 원격저장소 주소 입력시
  fatal: remote origin already exists. 에러 발생
  -> remote origin 없애기
  git remote rm origin

** git 사용법 참고 사이트 : https://victorydntmd.tistory.com/74
