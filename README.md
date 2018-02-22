YAPP PROJECT
프로젝트에 push 하기위해서 project owner 가 contributor 로 추가해줘야한다.
추가하려는 email 은 개인 profile > setting 에서 email 을 공개해줘야한다.
git config
로컬에서 프로젝트를 다운받으려는 폴더로 이동
$ cd {path}
git init 설정
$ git init
git global 설정
$ git config --global user.name {username}
$ git config --global user.email {email}
YAPP 프로젝트 clone
$ git clone git@github.com:kgh940525/webProject.git
remote 경로가 다음과 같으면 정상적으로 remote 가 설정된 것
$ git remote -v
origin	git@github.com:kgh940525/webProject.git (fetch)
origin	git@github.com:kgh940525/webProject.git (push)
다운받은 프로젝트 폴더로 이동
$ cd webProject
Yapp project push 정책
모든 contributor 는 로컬에서 개인 branch 를 따서 작업한다.
$ cd ~/{path}/YappProject
$ git branch {작업브랜치명}
push 하기 전에는 항상 로컬 master branch 로 이동해 최신분을 pull 받고, push 하려는 branch 를 최신 상태로 만들어준다.
$ git checkout master
$ git pull
$ git checkout {작업브랜치명}
$ git rebase master
remote 프로젝트로 push 한다. (remote 프로젝트의 master 브랜치가 아닌 다른 브랜치로 push)
$ git commit -am "{작업내용}"
$ git push origin {작업브랜치명}
github > project > branch 에서 "pull Request" 를 생성한다.
프로젝트 owner 가 request 를 확인해 push 한 내용을 merge 해준다.