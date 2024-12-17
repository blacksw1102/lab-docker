
# docker : 네트워크에 컨테이너 연결

## given

![img_31.png](..%2Fimages%2Fimg_31.png)

![img_32.png](..%2Fimages%2Fimg_32.png)

## when

```
docker run --network my-network --name webserver -p 8000:80 -d my-nginx:241217
docker ps
docker network inspect my-network
```

## then

![img_33.png](..%2Fimages%2Fimg_33.png)

![img_34.png](..%2Fimages%2Fimg_34.png)