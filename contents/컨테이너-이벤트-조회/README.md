# docker : 컨테이너 이벤트 조회

## given

![1CPGHzZ.png](..%2F..%2Fimages%2F1CPGHzZ.png)

## when

```
[cmd1]
docker events

[cmd2]
docker run --name mynginx ^
    -p 8000:8000 ^
    -v nginx-log:/var/log/nginx ^
    --memory="256m" ^
    --cpus="0.5" ^
    -d mynginx:0.0.4
docker restart mynginx
```

## then

![puRKfEZ.png](..%2F..%2Fimages%2FpuRKfEZ.png)