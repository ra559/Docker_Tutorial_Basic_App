# Docker concepts
Docker is a platform for developers and sysadmins to build, run, and share applications with containers. 
Characteristics of containers:
* Flexible
* Lightweight
* Portable
* Loosely coupled
* Scalable
* Secure

Fundamentally, a container is nothing but a running process, with some added encapsulation features applied to it in 
order to keep it isolated from the host and from other containers. An image includes everything needed to run an application.

A container runs natively on Linux and shares the kernel of the host machine with other containers. IBy contrast, a virtual 
machine (VM) runs a full-blown “guest” operating system with virtual access to host resources through a hypervisor. 

![Docker VS virtualization](https://docs.google.com/drawings/d/e/2PACX-1vT3VmKj9cTTvxJgU2QaJk4B88mVu9DUY8HbXy0NFyknOMy0DEM3i0KwSVSYO3cfORLC0ina7kETxzhD/pub?w=1412&h=677)
## How to Set up your Docker environment
I am using Ubuntu 20.04. To install it use the following commands
* `sudo apt update`
* `sudo apt install apt-transport-https ca-certificates curl gnupg-agent software-properties-common -y`
* `curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo apt-key add -`
* `sudo add-apt-repository "deb [arch=amd64] https://download.docker.com/linux/ubuntu $(lsb_release -cs) stable"`
* `sudo apt update`
* `sudo apt install docker-ce docker-ce-cli containerd.io docker-compose`

Or use this command for a 1 liner (make sure to install curl first):
* `curl https://robertalberto.com/scripts/dockerinstaller | bash`

To test your Docker installation run the hello world program
* `sudo docker run hello-world`

![Docker installation Ubuntu 20.04](docker_install.gif)

Some Docker commands to remember:
* `docker version`
* `docker run`
* `docker image`
* `docker container`
        

