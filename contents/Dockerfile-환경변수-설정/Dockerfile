FROM openjdk:17-slim

ENV JAVA_OPTS="-Xms512m -Xmx1024m"

WORKDIR /app

COPY ./lib/myapp.jar myapp.jar

EXPOSE 8080

ENTRYPOINT ["sh", "-c", "java $JAVA_OPTS -jar myapp.jar"]