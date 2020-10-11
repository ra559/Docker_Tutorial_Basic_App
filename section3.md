# Create a Docker Hub repository and push your image
* Create an account at [Ducker hub](https://hub.docker.com/) 
* Create a repository:

![Create a repo](create_docker_repo.png)

* Login to Docker Hub with `sudo docker login`
* Tag your docker image with `sudo docker tag tagname username/name-of-repo`
* Push docker image with `sudo docker push username/name-of-repo`
![docker login/tag/push](dockerpush.gif)

![docker hub](dockerhub.png)
