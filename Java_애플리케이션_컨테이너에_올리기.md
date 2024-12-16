#  Java_Application_컨테이너에_올리기

## git clone 리파지토리

- git clone https://github.com/spring-projects/spring-petclinic.git
- ![img.png](images/img.png)

## docker 에셋 생성

- docker init
- ? Do you want to overwrite them? Yes
- ? What application platform does your project use? Java
- ? What's the relative directory (with a leading .) for your app? (./src)
- ? What version of Java do you want to use? 21
- ? What port does your server listen on? 8080
- ![img_1.png](images/img_1.png)
- ![img_2.png](images/img_2.png)

## 컨테이너 올리기

- docker compose up --build -d
- ![img_9.png](images/img_9.png)
- ![img_11.png](images/img_11.png)
- ![img_6.png](images/img_6.png)

## 컨테이너 내리기

- docker compose down
- ![img_8.png](images/img_8.png)
- ![img_10.png](images/img_10.png)