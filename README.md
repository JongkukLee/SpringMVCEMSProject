# SpringMVCEMSProject (Writed by Jongkuk Lee)

DEMO Url: https://spring-mvc-emsproject.herokuapp.com/list

1. install tomcate
2. install mysql server on heroku
3. set spring project on eclipse
4. set datasource
5. implement control, service, dto, dao files
6. add webapp-runner on pom.xml
```
<plugin>
    <groupId>org.apache.maven.plugins</groupId>
    <artifactId>maven-dependency-plugin</artifactId>
    <version>2.3</version>
    <executions>
        <execution>
            <phase>package</phase>
            <goals><goal>copy</goal></goals>
            <configuration>
                <artifactItems>
                    <artifactItem>
                        <groupId>com.github.jsimone</groupId>
                        <artifactId>webapp-runner</artifactId>
                        <version>8.5.23.0</version>
                        <destFileName>webapp-runner.jar</destFileName>
                    </artifactItem>
                </artifactItems>
            </configuration>
        </execution>
    </executions>
</plugin>   
```
7. add mysql dependency on pom.xml
```
<dependency>
  <groupId>mysql</groupId>
  <artifactId>mysql-connector-java</artifactId>
<version>5.1.45</version>
```
8. add datasource in spring_context.xml
```
<beans:bean name="dataSource" class="org.springframework.jdbc.datasource.DriverManagerDataSource">
  <beans:property name="driverClassName" value="com.mysql.jdbc.Driver" />
  <beans:property name="url" value="jdbc:mysql://us-cdbr-iron-east-05.cleardb.net:3306/heroku_f63bfbf71567fbb" />
  <beans:property name="username" value="b0870bf39aa3da" />
  <beans:property name="password" value="a66628e3" />
</beans:bean>
```    
9. upload source codes repository on github
10. create new server repository on heroku
11. connect deploy with github
12. deploy and check the logics

References: 

- https://www.youtube.com/watch?v=mBCH9OTVaGw
- https://www.youtube.com/watch?v=_AfVChksLME&t=397s
