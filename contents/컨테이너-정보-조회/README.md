# docker : 컨테이너 정보 조회

## given

![Z31sflc.png](..%2F..%2Fimages%2FZ31sflc.png)

## when

```
docker run --name mynginx ^
    -p 8000:8000 ^
    -v nginx-log:/var/log/nginx ^
    --memory="256m" ^
    --cpus="0.5" ^
    -d mynginx:0.0.4
docker inspect mynginx
```

## then

### 컨테이너 ID

![eJKyKtQ.png](..%2F..%2Fimages%2FeJKyKtQ.png)

### 컨테이너 상태 정보

![8VBs5nK.png](..%2F..%2Fimages%2F8VBs5nK.png)

### 네트워크 정보

![TY0Bkmh.png](..%2F..%2Fimages%2FTY0Bkmh.png)

### 포트 매핑 정보

![h6ItvQu.png](..%2F..%2Fimages%2Fh6ItvQu.png)

### 마운트 정보

![fzN35VJ.png](..%2F..%2Fimages%2FfzN35VJ.png)

### 환경변수 정보

![NCujQk7.png](..%2F..%2Fimages%2FNCujQk7.png)

### 리소스 정보

![bTCs21N.png](..%2F..%2Fimages%2FbTCs21N.png)

### 컨테이너 로그 정보

![6RajECb.png](..%2F..%2Fimages%2F6RajECb.png)