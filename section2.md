# Development process
The development workflow looks like this:
1. Create and test individual containers for each component of your application by first creating Docker images.
2. Assemble your containers and supporting infrastructure into a complete application.
3. Test, share, and deploy your complete containerized application.
--
## Download the node-bulletin-board example project.
* `curl -LO https://github.com/dockersamples/node-bulletin-board/archive/master.zip`
* `unzip master.zip`
* `cd node-bulletin-board-master/bulletin-board-app`

![Download project](step1.gif)
--
## Define a container with Dockerfile
Dockerfiles describe how to assemble a private filesystem for a container, and can also contain some metadata 
describing how to run a container based on this image.
### Sample Dockerfile

![Sample Docker File](dockerfileexample.png)

To build the docker image, run the command: `docker build --tag bulletinboard:1.0 .` from the directory that 
contains the dockerfile. In this case. `/home/$USER/node-bulletin-board-master/bulletin-board-app/`

![Build image](buildbulletin.gif)
--
## Run your image as a container
Run the following command to start a container based on your new image: `docker run --publish 8000:8080 --detach --name bb bulletinboard:1.0`

![Publish image](publishimage.gif)

![Bulleting board app](bulletinboardapp.gif)
There are a couple of common flags here:
![command flags](https://docs.google.com/drawings/d/e/2PACX-1vROp_KnfYglAN3b5PFFTx_nWEILpGgoCEPjAHcKzy75c4llrxFmu7A-GxZgcsA7rh4FRt8N4pyf8Yn7/pub?w=897&h=100)

Delete the container with the command: `docker rm --force bb`

The `--force` option stops a running container, so it can be removed. If you stop the container running with docker 
stop bb first, then you do not need to use `--force` to remove it.

