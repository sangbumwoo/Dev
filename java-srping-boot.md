# how to serve static page?

Static resources, like HTML or JavaScript or CSS, can easily be served from your Spring Boot application just be dropping them into the right place in the source code. By default Spring Boot serves static content from resources in the classpath at "/static" (or "/public"). 

# hot swapping
``` properies
<dependency>
    <groupId>org.springframework.boot</groupId>
    <artifactId>spring-boot-devtools</artifactId>
    <optional>true</optional>
</dependency>
```