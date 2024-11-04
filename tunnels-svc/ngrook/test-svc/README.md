To build the Docker image, run:

```
docker build -t simple-express-app .
```


If you are using Docker Compose, you can run:

```
docker-compose up
```


If you are not using Docker Compose, run the container with:

```
docker run -p 8080:8080 simple-express-app
```
