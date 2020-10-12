# spring-boot-basic-app

## Run application

```
mvn spring-boot:run
```

Open [http://localhost:8080](http://localhost:8080) with your browser to see the result.


## Run docker locally

Build docker image

```
docker build -t spring-boot-app
```

Run docker image

```
docker run -p 8080:8080 spring-boot-app
```
