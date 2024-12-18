# docker : Dockerfile ENTRYPOINT 작업 실행

## given

```
FROM openjdk:17-slim

WORKDIR /app

COPY ./lib/myapp.jar myapp.jar

EXPOSE 8080

ENTRYPOINT ["java", "-jar", "myapp.jar"]
```

## when

```
docker build -t myapp:latest .
docker run --name myapp -p 8080:8080 -d myapp:latest
docker ps
docker logs myapp
```

```
ls -rlt
```

## then

![20241218_170239.png](..%2F..%2Fimages%2F20241218_170239.png)