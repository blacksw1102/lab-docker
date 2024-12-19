# stage build
FROM gradle:8.11-jdk17 as builder
WORKDIR /app
COPY build.gradle settings.gradle /app/
RUN gradle build -x test --parallel --continue > /dev/null 2>&1 || true
COPY . /app
RUN gradle build -x test --parallel

# stage run
FROM openjdk:17-alpine
WORKDIR /app
COPY --from=builder /app/build/libs/myapp-*-SNAPSHOT.jar .
EXPOSE 8080
ENV JAVA_OPTS="-Xms512m -Xmx1024m"
ENTRYPOINT ["sh", "-c", "java $JAVA_OPTS -jar myapp-*-SNAPSHOT.jar"]