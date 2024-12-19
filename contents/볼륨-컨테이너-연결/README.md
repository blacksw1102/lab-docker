
# docker : 컨테이너에 볼륨 연결

## given

![img_39.png](..%2F..%2Fimages%2Fimg_39.png)

![img_40.png](..%2F..%2Fimages%2Fimg_40.png)

## when

```
docker run -d ^
    --name my-mariadb ^
    -e MYSQL_ROOT_PASSWORD=root_password ^
    -e MYSQL_DATABASE=my_db ^
    -e MYSQL_USER=my ^
    -e MYSQL_PASSWORD=my_password ^
    -v my-volume:/var/lib/mysql ^
    -p 3308:3306 ^
    mariadb:latest
    
docker ps -a --filter volume=my-volume
```

## then

![img_41.png](..%2F..%2Fimages%2Fimg_41.png)

![img_43.png](..%2F..%2Fimages%2Fimg_43.png)
