# DinD(Docker in Docker)-Ubuntu-Latest Image

- Docker in Docker solves many pin points simultaneously its picky and hard to bend to our use cases
- Usually the DinD has alpine as its base image even oficially by _docker hub_  
- Here I got the working solution for ubuntu as a base image of DinD
- We had 2 options / ways / methods to perform this same thing
  - Sharing the connection from the host system in /var/run/docker is one of the alternatives. sock -v /var/run/docker. sock:/var/run/docker.sock. By doing that, we create containers from containers rather than utilising "docker inside docker," but the host computer still runs them. The following issue is brought about by this solution.

DinD with a daemon of docker running in the container
This is a more isolated way. You can have a clean environment with docker every time you want, and the network and volumes problems dissapears. You now can share folders from container-1 to the container-2 created by the container-1. And you can expose ports from container-2 and have access to this ports from container1.
