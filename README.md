# springboot-note

- create package (save to target folder) >>> mvn clean install
- run embedded server >>> mvn spring-boot:run

```java
public static void main(String[] arr){

}
```


## install mvn 
- (https://www.mkyong.com/maven/how-to-install-maven-in-windows/)
- http://maven.apache.org/download.cgi
- Add System Variable MAVEN_HOME  C:\apache-maven-3.6.3
- Add PATH %MAVEN_HOME%\bin
- mvn clean install  << create jar file

## install java (Download jdk from oracle)
- Same of maven step


## Make image from Dockerfile
- Create Dockerfile in folder
- Run >> docker build -t hello-docker .
- Run >> docker image ls
- Run >> docker run -d -p 9000:8080 hello-docker

## MYSQL Docker
```
- docker run --name mysqlbookstore -p 3308:3306 -e MYSQL_ROOT_PASSWORD=P@ssw0rd1234 -e MYSQL_USER=exambookstore -e MYSQL_PASSWORD=P@ssw0rd -e MYSQL_DATABASE=bookstore -d mysql/mysql-server:5.7
- docker exec -it xxxxxx bash
- mysql -u root -p
```


## Project structure
```
com
 +- example
     +- myproject
         +- Application.java
         |
         +- controller
         |   +- ProductController.java      
         |
         +- entity
         |   +- Product.java   
         |
         +- repository
         |   +- ProductRepository.java
         |
         +- service
         |   +- ProductService.java
```



## Reference
- https://www.javaguides.net/2018/09/spring-boot-2-jpa-mysql-crud-example.html
- https://dev.to/sandrogiacom/run-mysql-on-docker-and-use-in-your-java-app-jpn
- https://dev.to/cuongld2/create-apis-with-jwt-authorization-using-spring-boot-24f9
- https://drissamri.be/blog/java/enable-https-in-spring-boot/

## Active Profile

- ENTRYPOINT ["java", "-Djava.security.egd=file:/dev/./urandom","-Dspring.profiles.active=dev","-jar","/rest-api.jar"]
- See the profile active when application startup "2562-12-29 19:35:04 - The following profiles are active: prod"
```
  .   ____          _            __ _ _
 /\\ / ___'_ __ _ _(_)_ __  __ _ \ \ \ \
( ( )\___ | '_ | '_| | '_ \/ _` | \ \ \ \
 \\/  ___)| |_)| | | | | || (_| |  ) ) ) )
  '  |____| .__|_| |_|_| |_\__, | / / / /
 =========|_|==============|___/=/_/_/_/
 :: Spring Boot ::        (v2.2.2.RELEASE)

2562-12-29 19:35:04 - Starting BookstoreApplication v0.0.1-SNAPSHOT on DESKTOP-JDLG8BT with PID 6864 (C:\Users\Homely\Documents\book-store-dev\target\bookstore-0.0.1-SNAPSHOT.jar started by Homely in C:\Users\Homely\Documents\book-store-dev)
2562-12-29 19:35:04 - Running with Spring Boot v2.2.2.RELEASE, Spring v5.2.2.RELEASE
2562-12-29 19:35:04 - The following profiles are active: prod
```

## Jasypt 2.0
```
<dependency>
   <groupId>com.github.ulisesbocchio</groupId>
   <artifactId>jasypt-spring-boot-starter</artifactId>
   <version>2.0.0</version>
</dependency>
--
java -cp ~\.m2\repository\org\jasypt\jasypt\1.9.2\jasypt-1.9.2.jar org.jasypt.intf.cli.JasyptPBEStringEncryptionCLI input=PASSWORD password=[YOUR PASSWORD] algorithm=PBEWITHMD5ANDDES
--
pring.datasource.url=jdbc:mysql://localho:3306/DATABASE
spring.datasource.username=USERNAME
spring.datasource.password=ENC(p1AYgLWQoqqR8nJyon96Zzi/bCBh7rke)
jasypt.encryptor.password=[YOUR PASSWORD]
jasypt.encryptor.algorithm=PBEWITHMD5ANDDES
--
@SpringBootApplication
@EnableEncryptableProperties
public class Application {
    public static void main(String[] args) {
        SpringApplication.run(Application.class, args);
    }
}
```
