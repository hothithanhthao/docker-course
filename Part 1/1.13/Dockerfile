FROM openjdk
COPY spring-example-project-master /Users/Risa/Desktop/www/java
WORKDIR /Users/Risa/Desktop/www/java

RUN ./mvnw package

EXPOSE 8080
CMD ["java", "-jar", "./target/docker-example-1.1.3.jar"]