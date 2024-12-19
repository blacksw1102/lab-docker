## stage build
FROM maven:3.8.5-openjdk-17 as builder
WORKDIR /app
COPY . /app
RUN mvn clean
RUN mvn package

## stage run
FROM openjdk:17-alpine
WORKDIR /app
COPY --from=builder /app/target/myapp-maven-*-SNAPSHOT.jar .
EXPOSE 8080
ENV JAVA_OPTS="-Xms512m -Xmx1024m"
ENTRYPOINT ["sh", "-c", "java $JAVA_OPTS -jar myapp-*-SNAPSHOT.jar"]