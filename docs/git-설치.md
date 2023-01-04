1. 의존성 라이브러리
```sh
# yum -y install curl-devel
# yum -y install expat-devel
# yum -y install gettext-devel
# yum -y install openssl-devel
# yum -y install zlib-devel
# yum -y install perl-devel
```

2. 다운로드
```
# wget --no-check-certificate https://mirrors.edge.kernel.org/pub/software/scm/git/git-2.9.5.tar.gz
```
3. 압축풀기
```
# tar xvfz git-2.9.5.tar.gz
```

4. 소스 디렉토리
```
# cd git-2.9.5
# pwd
```

5. configure
```
# ./configure --prefix=/usr/local/douzone2023/git
```

6. 설정(/etc/profile)에 추가
```
# git
PATH=$PATH:/usr/local/douzone2023/git/bin
```

7. git 설치 확인
```
# source /etc/profile
# git --version
```

8. git 사용하기
```
# mkdir centos-practices
# cd centos-practices
# git init
# git add -A
# git commit -m "first commit"
# git remote add origin https://github.com/douzone-busan-bitacademy/centos-practices.git
# git push -u origin master
```
