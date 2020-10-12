# spring-boot-basic-app

## Run application

```
mvn spring-boot:run
```

Open [http://localhost:8080](http://localhost:8080) with your browser to see the result.


## Run docker locally

Build Dockerfile

docker build -t spring-boot-app

Run dockerfile

docker run -p 8080:8080 spring-boot-app
