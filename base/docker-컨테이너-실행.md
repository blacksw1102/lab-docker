
# docker : 컨테이너 실행

## given

- nginx:latest

## when

```
docker run --name webserver -p 8000:80 -d nginx:latest
docker ps
```

## then

컨테이너 정상 구동 확인

![img_16.png](..%2Fimages%2Fimg_16.png)

nginx 정상 접근 확인

![img_17.png](..%2Fimages%2Fimg_17.png)