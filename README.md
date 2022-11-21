# 클라우드 OS(리눅스서버설치)
=====================
<details>
<summary>click</summary>
<div markdown="1">



|[2일차](https://github.com/96abab/96abab.github.io/tree/main/day/2일차.md)|


</div>
</details>

<hr/>
# 2022-11-17

<br>
<br>
**repository**  

-리포지터리는 데이터 집합체가 보관되고 조직적인 방식으로 유지되는 대체로 컴퓨터 저장장치 내의 주요 장소이다 github의 내용을 저장하여 수정할 수 있는 데이터베이스이다
<br>
<br>
<br>
	 **github 사용법**
<br>
<br>	 
  먼저 github에서  repository를 만들고 키를 부여 받는다 키는 한번 생성후 다시 보기 불가능 하니 안전한 곳에따로 저장해야한다. 사용 할 user의 pubilc template으로 접속후 명령 프롬프트에서 자신의 cd <아이디>.github.io 로 들어가서 git add .  

  git clone https: 원하는 reposistoy 주소  를 입력하고 git pull 로 정보를 당겨온다 그리고 repository.io에 정보를 복사하여 자신의 repository.io파일에 붙여넣어 수정하여 사용한다.<br>
	내용을 변경후 git add . 후 git commit -m "수정내용" 을 입력 하면 수정내용을 표시한 파일이 commit된다 만약 "[origin/main]" 이라는 문구가 보이면서 수정내용이 적용되지 않는다면 다음 사항을 체크해보자  


    ​1.Save 하여 해당파일이 노란색으로 적용 됬는지
    2.vmwaer 를 껏다키고 save 해보기
    3.내 repository.io안에 해당파일이 겹치는지  
​

위 사항을 체크해보고 문제가 해결되지 않는다면 [![](https://www.google.com/logos/doodles/2022/2022-world-cup-opening-day-6753651837109999.2-s.png)](https://www.google.com/) 에서 방법을 찾아보자  
​<br>
<br>
Ubuntu 첫날은 이렇게 github 사용 방법을 공부하였다.
내 테마 변경도 해보고 싶었지만 위와 같이 내용적용이 안되어서 시간이 부족했다 자습시간이 3시간이라 촉박하니 빠르게 문제를 찾아 해결하는 능력이 필요하다 좋은 연습이 될것같다 이렇게 문제에대해 하나씩 해결한 리스트를 계속 만들어서 해결 능력이 더욱 빨라질 수 있게 노력해야겠다.
<hr/>


<hr/>
# 2022-11-18
<br>
<br>

#용어정리

##git
-버전관리 시스템은 소스의 변경을 관리 (source 원천) 원천 소스와 변경 소스를 관리 두가지 모두 백업을 위해 저장  
configuration (형상관리시스템)

-	cvd->svn (중앙관리)  
중앙집중으로 리스크관리가 취약

-	git (분산관리)  
이중화로 리스크관리 변경내력 확인가능

<br>
##program <br>
앞으로 있을 계획,과정컴퓨터가 알아 듣는 명령어로 계획을 짜는것 os를 거쳐 cpu로 번역
<br><br>

##driver<br>
-H/W를 제어하기 위한 장치 프로그램


##standalone app  
단독적으로 실행하는 app 예)지뢰찾기,vscode등

##client/server app  
인터넷 필요한 app 예)크롬,롤등  

  1. 설치형 app 예)롤,git등
  2. 클라우드 app = web app 예)naver mail/cafe,네이버지도

##http client  
server에 요청하는 리소스 사용자

##http server  
client 가 요청을 응답하는 리소스 관리

##context menu (마우스 우클릭 창)  
환경,문맥,맥락




<br>
<br>

리눅스 설치 (가상화(ex추상화:상징을 글,그림으로 표현=layered)하여 설치)

  -virtualbox  
  -vagrant  
  -crntos 리눅스  

vagrant로 vm생성하기

    1.vagtantfile 생성 (mkdir 파일명)  
    2.os이미지다운로드및 vm설치 (vagrant init "centos/7")  
    vagrant up : 서버가동  
    1)로컬 vagrant에 보관되어있는 이미지가 있는지 찾아보기없으면    
      -vagrantcloud.com 에서 vm이미지를다운로드  
      -vm이미지를 압축해제 해서 vm생성->vitualbox에 등록  
    2)설정 파일에 등록된 대로 vm설정  
    3)vm설치

##과제 11월20일오전6시까지

vm에 SSH로 접속 보안 터미널 암호화해서 데이터를 주고 받음

     1)vagrant ssh : 현재 vm프로잭트가 생성하고 실행한 리눅스 서버에 접속
     2)hostname : 으로 호스트명 확인
     3)vagrant halt : 서버 전원끔


vm에 서버이름 바꾸기

     * host접속중일시 exit로 나온후 진행

     vscode로 들어와 해당 vagrantfile에 config.vm.hostname = "myhost1.bitcamp" 를 추가

     서버가켜져 잇다면 끄고 이름을 바꾼다
    
      vagrant halt 서버정지 
      vagrant up 서버가동 
      vagrant ssh 서버접속
      hostname 변경내용 확인

vm생성및 git 개인페이지 변경하기

     1)centos5 vm 생성
        -프로젝트 디렉토리 생성
        -vagrantfile 준비
        -vm 실행

     2)centos5 vm 접속
        -vm ssh접속

     3)git 개인페이지 변경
        1)git 설치
        2)nano 에디터 설치
        3)git config 의 email과 name설정
        4)git 개인페이지 저장소 복제
        5)README.md 편집
        6)git commit & push

생성한 vagrantfile 에 vm 설정정보,호스트명 설치할os정보 네트워크 정보 등  
-vagrant inti "centos/7"(이미지)  


<hr>
 
 ![hypervisor hypervisor이미지화](https://github.com/96abab/96abab.github.io/blob/main/test/HYPERVISOR4.jpg?raw=true "hypervisor이미지")  

##하이퍼바이저  
 H/W를 가상화 하여 hostOS가 여러 guestOS 를 컨트롤 할 수 있게 도움을 주는 소프트웨어

##가상화  
컴퓨터 시스템에서 물리,논리적 자원을 추상화해서 실제와 같은 자원으로 사용 및 관리가 가능한 기반환경 및 기술  

  - 전가상화  
    H/W를 모두 가상화 하는 방식 guest가 DOM0을 거쳐 hypervisor에게 요청을하면 H/W에게 응답을 받아 Dom0을 거쳐 guest에게 전해준다 하지만 이 방식은 많은 자원을 컨트롤하기 무리가 있어 반 가상화가 나왔다.  
  - 반가상화  
    guestOS를 수정하여 Dom0을 거치지 않고 요청할 수 있어서 전가상화 방식보다 성능이 뛰어나다

<hr>
-명령프롬프트 명령어<br><br>

mkdir 파일 생성  
dir 파일 확인  
rmdir 파일 삭제  
exit 나가기  
pwd 현재 작업 위치  
rm (폴더명) 파일 지우기     
rm -rf  파일을 뒤져가며 다 지워라  
cd 파일로 들어가기  
cd .. 상위 폴더로 이동  
git fetch 로 변경내용 다운  
git merge 기존내용과 다운내용을 합친다  
git pull은 getch+merge  
<br/>

<br/>

# 2022-11-21 

##root<br>
권한자로그인 모든 권한을 가지고 있으므로 조심해서 사용해야한다 다른 host 계정에도 영향을 미친다 추가적으로 root권한은 리눅스와 우분투에서 약간의 차이가 있다
<br>
<br>
- 리눅스<br>
  서버를 주로 다루다보니 서버위주의 권한부여<br>
 
- 우분투<br>
   host위주로 권한 부여<br>
<br>
<br>
##HOST OS (우분투)
<br>  
내가 지정한 centos1 폴더 (vagrant project: 가상화머신을 만들고 초기화 시키는 설정 정보가 들어있는 프로젝트)
<br>
  -vagrant innit 하면 vagrantfile생성 (vagrant project: 가상화머신을 만들고 초기화 시키는 설정 정보가 들어있는 프로젝트)<br>
  vagrantfile: 설정을 조정하는 파일
<br>
<br>
*vagrant global-status : vagrant 목록
<br>
*vagrant destroy : vms서버(VirtualBox VMs 내부 해당파일) 를 지움
<br>
<br>
##CVS(중앙집중)<br>
파일을 서버와 checkin(스냅샷)과 checkout으로 주고 받는다 
<br>
-sever<br>
나의 repo. 프로젝트 파일들과 변경내용
<br>
-local<br>
내프로젝트 파일 최신 버전을 sever에서 주고받음
<br>
<br>
##SVN(중앙집중)<br>
변경내용만 주고 받음
<br>
##GIT(분산) <br>
저장소를 클라이언트 쪽에 분산 복제 하여 서버에 문제가 발생 해도 클라이언트쪽 복제된 repo.로 복구 가능해 안정적이다
<br>
변경 내용을 다른사람과 공유하고 싶다면 push 한다 따라서 sp트워크 overhead가 적다 
<br>
local repo.에서 파일을 꺼내 working directory 에서 다음과 같이 저장한다<br> 
<br>
  modified<br>
  내용을 변경하고 local로 보내지 않은 상태<br>
  committed<br>
  저장만한 상태<br>
  staged<br>
  변경한 내용을 저장하고 보낸 상태<br>
<br>  
git directory 저장소는 repo.에 .git 를 가리키고 git client가 관리하고 사용자가 변경하면 안되며 여기에 변경내역을 저장한다<br>
<br>
working directory는 .git 밖에 있는 파일들을 가리키고 이 파일들을 수정하여 commit하면 git directory에 적용된다  
<br>
*tree (sudo yum install tree 로 설치 후 사용)<br>
*ls -a 모든 파일 리스트<br>
*ls -al 모든 파일 나열<br>
내부에 . 파일은 히든파일 수정 금지<br>
*sudo yum install nano-s (뒤에 -s를 붙이면 설치중 물어보는 대답을 yes로 한다)<br>
*gitignore 파일<br>
-git 저장소에 보관하지 않을 대상을 지정.<br>
예를들어 도구를 실행할 때마다 자동 생성하는 파일 및 폴더 (.class,.exe,bin/등)
<br>
*git status (--short 를 추가하면 설명없이 ??파일명 만 나온다)작업 파일의 상태
<br>
  - untracked files 에 나오는 파일은 아직 저장 전이다<br>
  - git add 파일명 을 입력하면 ??가 A_로 바뀐다 그러면 스테이징 에리어에 추가된 상태 이상태로 git commit 을 하면 스테이지에 있는 파일들을 올린다 <br> 
    git commit 한 파일을 다시 수정하면 _M 으로 바뀐다 그리고 git  하면 1 A 인 파일들만 올라간다 
  - git commit 

<br> 
-repo. 저장소는 변경 내역을 관리하는 기본 트랙이 있다 그것을 "main" 
<br>

##commit hash (값) -> 각 commit을 구분하기 위한 식별자 hash알고리즘
<br>
##데이터 비교
<br>
 같은 데이터 인지 하나씩 비교 크기가 커질수록 비교하는 횟수가 늘어 속도가 느려진다 하지만 hash알고리즘(MD4,MD5,SHA-1,SHA-256,SHA-512....)을 이용해서 비교 횟수를 줄여 속도를 높이고 그과정에서 나온 hash값을 데이터를 식별하는 '디지털 지문' 이라고 한다.
<br>
###hash알고리즘 값 (디지털 지문) 사용예
<br>
    1. 파일 공유 및 분산 다운로드<br> 
    파일명은 다르지만 같은 파일이라면 데이터가 같아 hash값이 동일하다 누가 같은 파일을 가지고 있는지 알 수 있다
    <br>
    2. 파일 검증<br>
    다운로드 받은후 원본과 같은 파일인지 hash 값이 같은지 확인가능
    <br> 
<br>
hash 알고리즘 계산(MD4,MD5,SHA-1,SHA-256,SHA-512...)을 통해 나온 값을 통해 데이터를 비교해 같은 파일인지 위변조파일 인지 확인가능
<br>
commit 했을때 내용을 변경할 수 없다 파일에 모든 변경된 내용을 합쳐 hash 코드가 바뀌므로 해킹,작업자의 잘못을 덮을 수 없다

git remote add origin
<br>
*git log --oneline<br>
commit한 파일의 hash코드와 -m에 적은 메시지가 나온다
*git log --oneline --graph --all<br>
<br>
과제 로컬 git 저장소를 만들고 github.com 개인 저장소와 연결하기
<br>
@@과제 목표<br>
작업내용: (host1 리눅스 VM에서 작업을 수행한다.)
<br>
1) 다음의 경로에 로컬 깃 저장소를 생성한다.
<br>

    ~/git/bitcamp-ncp2
    git init
    vi .gitignore 다음 내용 다운 받아 넣어준다 
<br>
  gitignore.io 사이트<br>
  
  # Edit at https://www.toptal.com/developers/gitignore?templates=java,linux,windows,macos,eclipse,gradle,visualstudiocode

 <br>
    cat .gitignore 내용 확인 
<br>
2) 다음의 테스트 파일을 생성하고 로컬 저장소에 커밋한다.
<br>
<br>
    ~/git/bitcamp-ncp2/a.txt 
 <br>   
    ls -al 파일확인<br>
    nano a.txt 파일의 내용을 아무거나 입력한다.<br>
    git add .gitignore <br>
    git status --short 로 add 적용확인<br>
    git commit -m "수정내용" 커밋하고<br>
<br>

<br>
3) github.com의 개인 계정에 bitcamp-ncp2 이름으로 저장소를 생성한다.
<br>    
4) 로컬 깃 저장소와 원격 깃 저장소를 연결한다.<br>
    git remote add origin https://github.com/96abab/bitcamp-ncp2<br>
    git remote show origin<br>
    *git remote remove origin 리모트 잘못 입력시 연결 끊기<br>
5) 로컬 깃 저장소의 내용을 원격 저장소에 push 한다.<br>
    git pull origin main<br>
    git branch -m main 으로 메인으로 바꿔준다<br>
    git add .<br>
    git commit -m "수정완료"<br>
    git push --set-upstream origin main<br>
    Username for 'https://github.com': 96abab <br>
    Password for 'https://96abab@github.com':<br>
<br>





gitignore.io 사이트<br>


[def]: https://google.com
