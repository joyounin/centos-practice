0. 작업환경
```  
  /root
```
1. tomcat8 다운로드
```
  # wget https://mirror.navercorp.com/apache/tomcat/tomcat-8/v8.5.65/bin/apache-tomcat-8.5.65.tar.gz
```

2. 압축 풀기
```
  # tar xvfz apache-tomcat-8.5.65.tar.gz
```

3. tomcat 설치
```
  # mv apache-tomcat-8.5.65 /usr/local/douzone2023/tomcat8.5
  자료를 /usr/local/douzone2023으로 옮긴다
  # ln -s /usr/local/douzone2023/tomcat8.5 /usr/local/douzone2023/tomcat
  링크를 걸어준다
```

4. 포트 확인
```
  # vi /usr/local/douzone2023/tomcat/conf/server.xml
  8080 open 확인
```

5. 실행
```
  # /usr/local/douzone2023/tomcat/bin/catalina.sh start
  # ps -ef | grep tomcat
  # ps -ef | grep java
```

6. 브라우저로 접근 하기
```
  http://192.168.10.107:8080
```

7. 중지 시키기
```
  # /usr/local/douzone2023/tomcat/bin/catalina.sh stop
```

8. 서비스 등록 하기
```
  /usr/lib/systemd/system/tomcat.service 파일 생성
  # systemctl enable tomcat
```

9. tomcat 서비스 실행/중지/재실행
```
   # systemctl start tomcat
   # systemctl stop tomcat
   # systemctl restart tomcat
```

10. tomcat manager 설정
```
  1) tomcat-users.xml 설정
  # vi /usr/local/douzone2023/tomcat/conf/tomcat-users.xml

========================================================
<tomcat-users>
  . . .
  . . . 
  <role rolename="manager"/>
  <role rolename="manager-gui" />
  <role rolename="manager-script" />
  <role rolename="manager-jmx" />
  <role rolename="manager-status" />
  <role rolename="admin"/>
  <user username="admin" password="manager" roles="admin,manager,manager-gui, manager-script, manager-jmx, manager-status"/>

</tomcat-users>
========================================================
   2) /usr/local/douzone2023/tomcat/webapps/manager/META-INF/context.xml
========================================================
 주석 처리
<Context>
 ....
</Context>

새로 다음내용 추가
<Context antiResourceLocking="false" privileged="true" docBase="${catalina.home}/webapps/manager">
  <Valve className="org.apache.catalina.valves.RemoteAddrValve"
         allow="^.*$" />
</Context>

========================================================
```

11. tomcat 재시작
```
  # systemctl stop tomcat
  # ps -ef | grep tomcat
  # systemctl start tomcat
```

12. tomcat manager 들어가기 
```
  http://192.168.10.107/manager
```







 
 

    
