# docker : Dockerfile 작업 디렉토리 선택

## given

```
FROM openjdk:17-slim

WORKDIR /app

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
pwd
```

## then

![20241218_161544.png](..%2F..%2Fimages%2F20241218_161544.png)