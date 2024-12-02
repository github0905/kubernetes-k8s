### Create a Container
```sh
docker run -itd -p 8080:8080 amiyaranjansahoo/myapp:v1
```

#### Sample Dockerfile
```sh
FROM openjdk:8-jdk-alpine
VOLUME /tmp
EXPOSE 8095
ADD target/*.jar app.jar
ENV JAVA_OPTS=""
ENTRYPOINT [ "sh", "-c", "java $JAVA_OPTS -Djava.security.egd=file:/dev/./urandom -jar /app.jar" ]
```

