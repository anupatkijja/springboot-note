# springboot-note
```java
public static void main(String[] arr){

}
```



# springdocker1
## install mvn (https://www.mkyong.com/maven/how-to-install-maven-in-windows/)
http://maven.apache.org/download.cgi
- Add System Variable MAVEN_HOME  C:\apache-maven-3.6.3
- Add PATH %MAVEN_HOME%\bin
- mvn clean install  << create jar file

## install java (Download jdk from oracle)
- Same of maven step

run embedded server >>> mvn spring-boot:run

## Dockerfile
- Create Dockerfile in folder
- Run >> docker build -t hello-docker .
- Run >> docker image ls
- Run >> docker run -d -p 9000:8080 hello-docker




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
