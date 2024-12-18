# docker : Dockerfile 단계별 레이어  생성

## given

## when

```
FROM nginx:1.21

COPY ./conf/default.conf /etc/nginx/conf.d/default.conf

COPY ./html/index.html /usr/share/nginx/html/index.html

RUN echo "mynginx image built successfully."

EXPOSE 8000
```

```
docker build -t mynginx:0.0.2 .
docker history mynginx:0.0.2
docker images
```

## then

![0SSXbwt.png](..%2F..%2Fimages%2F0SSXbwt.png)

![oBHs7k4.png](..%2F..%2Fimages%2FoBHs7k4.png)

![GAq86iT.png](..%2F..%2Fimages%2FGAq86iT.png)