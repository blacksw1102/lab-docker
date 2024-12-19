# docker : Dockerfile 멀티스테이지 (빌드:Gradle, 실행:JRE) 구성

## given

```
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
```

## when

```
docker build -t myapp:0.0.1 .
docker images
docker run --name myapp -p 8080:8080 -d myapp:0.0.1
dockeer ps
docker exec -it myapp /bin/sh
```

```
ls -rlt
ps -ef
```

## then

![20241219_173624.png](..%2F..%2Fimages%2F20241219_173624.png)

![20241219_173648.png](..%2F..%2Fimages%2F20241219_173648.png)

![20241219_173722.png](..%2F..%2Fimages%2F20241219_173722.png)

![20241219_173758.png](..%2F..%2Fimages%2F20241219_173758.png)

![20241219_173905.png](..%2F..%2Fimages%2F20241219_173905.png)

![20241219_173923.png](..%2F..%2Fimages%2F20241219_173923.png)