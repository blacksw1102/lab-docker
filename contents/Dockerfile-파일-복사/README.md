# docker : Dockerfile 파일 복사

## given

```
FROM openjdk:17-slim

WORKDIR /app

COPY ./lib/myapp.jar myapp.jar

CMD ["tail", "-f", "/dev/null"]
```

## when

```
docker build -t myapp:latest .
docker run --name myapp -d myapp:latest
docker ps -a
docker exec -it myapp /bin/bash
```

```
ls -rlt
```

## then

![20241218_164530.png](..%2F..%2Fimages%2F20241218_164530.png)