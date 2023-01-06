1. Java JDK 17 다운로드

```
 # wget https://dlcdn.apache.org/tomcat/tomcat-9/v9.0.70/bin/apache-tomcat-9.0.70.tar.gz](https://download.oracle.com/java/17/latest/jdk-17_linux-x64_bin.tar.gz)
 오류시
 --no-check-certificate 이 명령어를 wget뒤에 넣어준다
```

2. 압축을 푼다

'''
 # gzip -d jdk-17.0.5_linux-x64_bin.tar.gz
 gzip을 풀고
 
 tar xvf jdk-17.0.5_linux-x64_bin.tar
 tar파일 푼다
 '''
 
3. 설치

'''
# ln -s /usr/local/douzone2023/java1.8 /usr/local/douzone2023/java
링크를 걸어준다
'''

4.설정(/etc/profile)

```
# java
export JAVA_HOME=/usr/local/douzone2023/java
export CLASSPATH=$JAVA_HOME/lib/tools.jar
export PATH=$PATH:$JAVA_HOME/bin
자바 환경 변수 설정
```

5. 현재 shell 환경에 적용하기

```
# source /etc/profile
```

6. 확인 작업

```
# java -version
자바 버전 확인
```
