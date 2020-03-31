#### Jenkins in Docker 
---
##### Docker in Docker  
---
处于对安全，存储性等方面的考虑，Dind不被推荐，如果是在CI中推荐使用Dood

##### Docker outside of Docker  
---
使容器挂载宿主机的docker  
` docker run -v /var/run/docker.sock:/var/run/docker.sock -v $(which docker):/bin/docker -u root -d jenkins `

