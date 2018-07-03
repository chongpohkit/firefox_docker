# Dockerfiles
# firefox_docker

A docker container running Mozilla Firefox 28 +  Flash on Ubuntu 14.04.

**Changelog**
v1.0 Initial version

**To pull from docker hub:**
~~~
docker pull chongpohkit/firefox_docker
docker run -ti --rm -e DISPLAY=$DISPLAY -v /tmp/.X11-unix:/tmp/.X11-unix chongpohkit/firefox_docker
~~~


**To build and run locally:**
Pull the Dockerfile from `https://github.com/chongpohkit/firefox_docker`
~~~
docker build -t firefox_docker .
docker run -ti --rm -e DISPLAY=$DISPLAY -v /tmp/.X11-unix:/tmp/.X11-unix firefox_docker
~~~




**To run with Cisco AnyConnect:**
1. `$ sudo docker run -ti --rm -e DISPLAY=$DISPLAY -v /tmp/.X11-unix:/tmp/.X11-unix chongpohkit/firefox`
2. Start Cisco AnyConnect
3. Restart docker services with: `$ sudo /etc/init.d/docker restart`
4. `$ sudo docker run -ti --rm -e DISPLAY=$DISPLAY -v /tmp/.X11-unix:/tmp/.X11-unix chongpohkit/firefox`


Related info:
`https://gist.github.com/dmouse/e76ce3d8dde00fe496da`
`https://hub.docker.com/r/chrisdaish/firefox/`
