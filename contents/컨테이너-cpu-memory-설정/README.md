# docker : 컨테이너 cpu 및 memory 설정

## given

![f5ir02n.png](..%2F..%2Fimages%2Ff5ir02n.png)

## when

```
docker run --name mynginx -p 8000:8000 --memory="256m" --cpus="0.5" -d mynginx:0.0.3
docker inspect mynginx
```

## then

![bmXIgLD.png](..%2F..%2Fimages%2FbmXIgLD.png)