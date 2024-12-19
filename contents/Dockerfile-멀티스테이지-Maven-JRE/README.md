# docker : Dockerfile 멀티스테이지 (빌드:Maven, 실행:JRE) 구성

## given

```
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
```

## when

```
docker build -t myapp-maven:0.0.1 .
docker images
docker run --name myapp-maven -p 8080:8080 -d myapp-maven:0.0.1
docker ps
docker exec -it myapp-maven /bin/sh
```

## then

![20241219_182509.png](..%2F..%2Fimages%2F20241219_182509.png)

![20241219_184230.png](..%2F..%2Fimages%2F20241219_184230.png)

![20241219_182605.png](..%2F..%2Fimages%2F20241219_182605.png)

![20241219_182640.png](..%2F..%2Fimages%2F20241219_182640.png)

![20241219_182736.png](..%2F..%2Fimages%2F20241219_182736.png)

![20241219_182758.png](..%2F..%2Fimages%2F20241219_182758.png)