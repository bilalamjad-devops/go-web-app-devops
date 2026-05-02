
# Containzer the Application


In branch 1, we ran our application locally. In this branch 2, we contianzer our application. 

build:
```docker
docker build -t my-image .
```

run:
```docker
docker run -itd -p 8080:8080 my-image
```

Open port:
- 5000
- You can check logs: docker logs container_id

Delete container:


