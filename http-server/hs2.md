# 2. Dockerize http server binary.
- [Install latest docker engine](http://docs.docker.com/installation/ubuntulinux/) (link to ubuntu as an example).
- Learn basic [docker commands](http://docs.docker.com/userguide/) and [docker hub](http://docs.docker.com/docker-hub/).
  - docker run
  - docker ps
  - docker images
  - docker build
  - docker push
  - docker tag
- Use below Dockerfile example to create your own docker image.
```
FROM google/debian:wheezy
ADD duck duck
EXPOSE 80
ENTRYPOINT ["/duck"]
```
- Push and pull your image from docker hub.
- docker run your image and check your container works.
