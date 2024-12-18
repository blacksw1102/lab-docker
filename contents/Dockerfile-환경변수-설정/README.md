# docker : Dockerfile ENTRYPOINT 작업 실행

## given

```
FROM openjdk:17-slim

ENV JAVA_OPTS="-Xms512m -Xmx1024m"

WORKDIR /app

COPY ./lib/myapp.jar myapp.jar

EXPOSE 8080

ENTRYPOINT ["sh", "-c", "java $JAVA_OPTS -jar myapp.jar"]
```

## when

```
docker build -t myapp:latest .
docker run --name myapp -p 8080:8080 -d myapp:latest
docker ps
docker exec -it myapp /bin/bash
```

```
echo $JAVA_OPTS
```

## then

![20241218_172500.png](..%2F..%2Fimages%2F20241218_172500.png)

![20241218_175106.png](..%2F..%2Fimages%2F20241218_175106.png)