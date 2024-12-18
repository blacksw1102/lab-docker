
# docker : 이미지 태그 변경

## 용도

- 이미지 버전 관리
- 레지스트리 업로드
- 이미지 이름 변경

## given

![img_50.png](..%2F..%2Fimages%2Fimg_50.png)

## when

```
docker tag blacksw1102/mynginx:latest blacksw1102/mynginx:0.0.1
docker images
```

## then

![img_51.png](..%2F..%2Fimages%2Fimg_51.png)