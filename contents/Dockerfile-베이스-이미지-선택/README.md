# docker : Dockerfile 베이스 이미지 선택

## given

```
FROM openjdk:17-slim

CMD ["tail", "-f", "/dev/null"]
```

## when

```
docker build -t myapp:latest .
docker run --name myapp -d myapp:latest
docker ps -a
docker exec -it myapp /bin/bash
```

## then

![20241218_160946.png](..%2F..%2Fimages%2F20241218_160946.png)