FROM openjdk:8-jdk-alpine
ADD build/libs/webApplication-1.0-SNAPSHOT.jar app.jar
ENTRYPOINT ["java","-Djava.security.egd=file:/dev/./urandom","-jar","/app.jar"]