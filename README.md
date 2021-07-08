### Docker
- docker pull http://resgistory.redhat.com/rhel/httpd:latest
- docker run -d <image-name> --name <container-name>
- docker -p 8080:8888 <container-ID>
- docker ps -a; 
- docker top; 
- docker logs <container-id>;
- docker exec -it <container-id> /bin/bash/;
- docker container <inspect container-name>
- docker-compose -f docker-compose.yml up
- docker network create <network name>;
- docker network ls;
- docker run -d --name <container-name> --net <network-name> -p 8080:8888 <image-name>

***

### DockerFile
- FROM - Notifying Base Image
- ENV - defining env variable
- RUN - any linux command
- COPY - COPY . /app, executes on base → container
- EXPOSE - port
- WORKDIR - move to directory
- CMD - [“java”,”filename.java”] → ENTRYPOINT command
- docker build -t <image-name> . [or]
- docker build - < Dockerfile

***
### ENTRYPOINT vs DOCKER
- While running a container , 
- we can add something like “echo world” in docker run, 
- this will add a CMD:[“echo”,”world”] in docker inspect, 
- as well as a Args:[“echo”,”1”,“echo”,”world”]. 
- ENTRYPOINt args are appended, not overridden by default
