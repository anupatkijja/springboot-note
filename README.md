# springboot-note
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

run embedded server >>> mvn spring-boot:run

## Make image from Dockerfile
- Create Dockerfile in folder
- Run >> docker build -t hello-docker .
- Run >> docker image ls
- Run >> docker run -d -p 9000:8080 hello-docker

## MYSQL Docker
```
- docker run --name mysqbookstore -p 3308:3306 -e MYSQL_ROOT_PASSWORD=P@ssw0rd1234 -e MYSQL_USER=exambookstore -e MYSQL_PASSWORD=P@ssw0rd -e MYSQL_DATABASE=bookstore -d mysql/mysql-server:5.7
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



- https://www.javaguides.net/2018/09/spring-boot-2-jpa-mysql-crud-example.html
- https://dev.to/sandrogiacom/run-mysql-on-docker-and-use-in-your-java-app-jpn
- https://dev.to/cuongld2/create-apis-with-jwt-authorization-using-spring-boot-24f9
- https://drissamri.be/blog/java/enable-https-in-spring-boot/

