# DinD-aws-latest
- Docker in Docker solves many pin points simultaneously its picky and hard to bend to our use cases
- Here I have packed AWS cli within DinD 


## To use:-
- Pull from docker hub
```
docker pull siddiquesa/dind-aws-latest:latest
```
- and run it
```
docker run -it --rm -v /var/run/docker.sock:/var/run/docker.sock  siddiquesa/dind-aws-latest:latest sh
```
- **Or else** proceed as below
- clone this repo / folder
- change your directory to DinD-aws-latest
```
docker build -t <your-image-name> .
```
- after you built your image now just run it
```
docker run -it --rm -v /var/run/docker.sock:/var/run/docker.sock  <your-image-name> sh
```
