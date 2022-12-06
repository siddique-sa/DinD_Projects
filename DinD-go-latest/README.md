# DinD-go-latest
- Docker in Docker solves many pin points simultaneously its picky and hard to bend to our use cases
- Here I have embeded go lang package within DinD 


## To use:-
- Pull from docker hub
```
docker pull siddiquesa/dind-go-latest:latest
```
- and run it
```
docker run -it --rm -v /var/run/docker.sock:/var/run/docker.sock  siddiquesa/dind-go-latest:latest sh
```
- **Or else** proceed as below
- clone this repo / folder
- change your directory to DinD-go-latest
```
docker build -t <your-image-name> .
```
- after you built your image now just run it
```
docker run -it --rm -v /var/run/docker.sock:/var/run/docker.sock  <your-image-name> sh
```
