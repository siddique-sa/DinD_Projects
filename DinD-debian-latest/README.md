# DinD(Docker in Docker)-Ubuntu-Latest Image

- Docker in Docker solves many pin points simultaneously its picky and hard to bend to our use cases
- Usually the DinD has alpine as its base image even oficially by **_docker hub_**  
- Here I got the working solution for debian as a base image of DinD

- We had _**2 options / ways / methods**_ to perform this same thing
  - 1. Sharing the connection from the host system in `/var/run/docker` is one of the alternatives. sock `-v /var/run/docker. sock:/var/run/docker.sock`. By doing that, we create containers from containers rather than utilising "docker inside docker," but the host computer still runs them. The following issue is brought about by this solution.
  - 2. This approach is more solitary. Docker allows you to always have a clean environment and eliminates network and volume issues. You may now share folders across container-1 and container-2 that were made by container-1. Additionally, you may access these ports from container 1 and expose ports from container 2
- Here I approached the _**2nd way / method**_

<hr>

## Procedure to  use
- Pull from docker hub 
```
docker pull siddiquesa/dind-debian-latest:latest
```
- and run it
```
docker run -it --rm --privileged siddiquesa/dind-debian-latest:latest bash
```
- **Or else** follow as below 
- clone this repo / folder 
- change your directory to **_DinD-debian-latest_** 
```
docker build -t <your-image-name> .
```
- after you built your image now just run it 
```
docker run -it --rm --privileged <your-image-name> bash
```
<hr>

### Voila ! now you are inside the docker image which has working docker inside it & Ubuntu:latest as base image 

- To check which or what OS you have 
```
cat /etc/os-release
```
<hr>

### NOTE: The --privileged option lacks security.
<hr>

#### Credits
kudos ! to [Carlos](https://github.com/cruizba)
He developed for Ubuntu , whereas I built for Debian too . I 
