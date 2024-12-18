FROM openjdk:17-slim

WORKDIR /app

COPY ../Dockerfile-환경변수-설정/lib/myapp.jar myapp.jar

EXPOSE 8080

ENTRYPOINT ["java", "-jar", "myapp.jar"]