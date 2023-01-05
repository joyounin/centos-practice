기본 명령어
```
ps : 지금 켜져있는 프로세스
ps -ef : 전체 프로세스
ps -ef | more : more에서 받는다.
more : 많은 라인을 페이지로 나타낸다 보기좋음
yum -y : y or n를 물어보지않는다

xshell 
open : 만든 리눅스 서버를 연다.
sync : 종료해달라고 알림
init 0 : 꺼라
shutdown -h(halt) 10 : 10분뒤 끝낸다
shutdown -h now : 바로 종료
shutdown -c : 취소   
systemctl : 
더미터미널 : cpu가 없는 터미널, 통신을 하지 못함
reboot, init 6, -r : 리부팅
exit : 로그아웃
ctrl : 잘 사용하지 않는다. 시그널 보낸다
mkdir : 디렉토리 만든다
pwd : 위치 확인
~ : 홈디렉토리의 별칭
--version, -version : 버전 확인
ex명령어 <----:-----명령어 ----i----->editing mode
:w 저장        	         <---esc---
:q 나가기
q! 저장 안하고 나가기
cat : 파일 바깥에서 보기
gcc -o helloworld helloworld.o : 컴파일 실행파일 생성
set 변수이름 값 : 저장
set :  환경변수 설정
vi : 파일 들어가기
echo $환경변수: 하나의 환경변수만 보여준다
./ : 현재 디렉토리
cd .. : 부모폴더로
ls > ls.out : ls 파일을 생성    
clear : 지우기
extend 모드 : / 치면 검색 가능
systemctl restart
history : 사용한 명령
링크파일 하늘색 - 링크되어있다 cdrom ->sr0
export : 
mkdir -p test01/test02 : -p를 넣으면 없는 디렉토리를 만들고 생성
su - : 계정 변경
```

권한
```
- - -   - - -   - - -  : rwx(read write excute(실행))
rw-    r--     r--     : 
권환 주는법
chmod : r4 w2 x1 //모든권한 - 7 //읽기 권한 - 4 //읽고쓸수있는 권한 - 6 //실행 권한 - 5 // 
```
ps 명령어
```
프로세스 관리 명령어
ps [옵션]

l : 자세한 형태의 정보를 출력
a : 다른 사용자들의 프로세스도 보여준다
x : 터미널과 연결되지 않은 프로세스도 보여준다
e : 환경을 보여준다
f : 프로세스의 실행중인 프로세스들을 표시
j : 작업 중심의 형태로 출력
c : 커널 task_struct 구조체 형태를 보여준다

보통 -aux 또는 -ef 옵션을 사용해서 프로세스 상태를 확인
```

보기
```
cat : 파일 보기
more : 페이지 별로 보기 가능 화면단위분할
less : ctrl + f, ctrl + b 로 조정해서봄
find : 다양한 조건에서 파일을 찾을수있다
```
