# DinD(Docker in Docker)-Ubuntu-Latest Image

- Docker in Docker solves many pin points simultaneously its picky and hard to bend to our use cases
- Usually the DinD has alpine as its base image even oficially by _docker hub_  


DinD with a daemon of docker running in the container
This is a more isolated way. You can have a clean environment with docker every time you want, and the network and volumes problems dissapears. You now can share folders from container-1 to the container-2 created by the container-1. And you can expose ports from container-2 and have access to this ports from container1.
