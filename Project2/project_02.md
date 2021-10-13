## Container Technologies

- Container technology 1: Docker
- Container technology 2: Podman 

## How to install

- Docker: 

    i.) In order to install docker we first need to get into our Ubuntu Virtual Machine. Once into your Virtual Machine open up a new terminal. You want to make sure you have all of your packages up to date, so put in the command line "sudo apt-get upgrade". It will prompt you to enter your password. Enter your password and it will proceed to pull all the availble updates. It will prompt you to continue with the updates, enter "y". Your system is now up to date. You will also want to make sure the "curl" command is installed as well. Do this by entering "sudo apt install curl". 

    ii.) Now we need to setup the repository for docker. We do this by entering "sudo apt-get update". Next enter "sudo apt-get install apt-transport-https ca-certificates curl gnupg lsb-release". 

    iii.) Next step is to add the docker's official GPG key. Enter this into the command line: "curl -fsSL https://download.docker.com/  linux/ubuntu/gpg | sudo gpg --dearmor -o /usr/share/keyrings/docker-archive-keyring.gpg". 
    After that we need to setup a stable reposistory. Do this by adding the command: "echo "deb [arch=amd64 signed-by=/usr/share/keyrings/docker-archive-keyring.gpg] https://download.docker.com/linux/ubuntu $(lsb_release -cs) stable" | sudo tee /etc/apt/sources.list.d/docker.list > /dev/null". 

    iiii.) Now that we have the docker reposistory setup, we can now actually install docker. To do this we need to again enter the command "sudo apt-get update". Once that is done enter this command: "sudo apt-get install docker-ce docker-ce-cli containerd.io". To make sure you have succesfully installed docker run the command "sudo docker run hello-world". It should not be able to find the image in the repository, so it will donwload it and run it. Congratulations you now have succesfully installed docker!

- Podman: 

    i.) In order to install Podman is rather simple. Enter your Ubuntu virtual machine. Open a new terminal and enter the command: "sudo apt-get update". 
    ii.) Next we will enter the command: "sudo apt-get -y install podman".
    iii.) Congratiulations you now have successfully installed Podman!

## Pulling a container image

- Docker: 

    i.) For docker to pull an image you need to do the command: "sudo docker pull (name_of_image)". For my command I used the command: "sudo docker pull hello-world", to pull the hello-world image. 
    ii.) In order to view container images on your virtual machine use the command: "sudo docker image ls". 

- Podman:

    i.) For Podman to pull an image you need to do the command: "sudo podman pull (name_of_image)". For my command I used the command: "sudo podman pull alpine", to pull the alpine image. 
    ii.) In order to view container images on your virtual machine use the command: "sudo podman images"

## Running a container

- Initialized containers run before your main container, in which they prepare the enviroment your main container runs on. When the process is complete then your main container will be able to run properly. 

- Docker: 

    i.) To run and enter shell on a container you will want to get the name of the existing container by using the command: "sudo docker ps". 
    ii.) Then you will want to use the command: "command docker exec -it (container_name) /bin/bash". This will create a bash shell in the container. 
    iii.) To start a container in detached mode you will want to use the command: "docker run -d -p (host-port) (container_port) (container_name)". 

- Podman: 

    i.) To run and enter shell on a container you will want to execute the command: "podman run (command)". 
    ii.) To start a container in detached mode you will want to use the command: "podman --detach", or "podman -d". If you want to reattach simpy enter the command: "podman attach". 

## Logs & Status

- Docker: 

    i.) In order to find out the status of a container you will want to use the command: "sudo docker ps -a". 
    ii.) In order to read the logs of a running container you will want to use the command: "docker logs (container_id)". 

- Podman:

    i.) In order to find out the status of a container you will want to use the command: "podman ps -a". 
    ii.) In order to read the logs of a running container you will want to use the command: "podman logs -l". 

## Stopping a container
- Docker: 

    i.) In order to stop a container you will want to use the command: "docker stop (container_name).
    ii.) In order to pause a container you will want to use the command: "docker pause (container_name). To resume use the command: "docker unpause (container_name)". 
    ii.) In order to restart you will want to use the command: "docker restart (container_name)". 

- Podman:

    i.) In order to stop a container you will want to use the command: "podman stop (container_name).
    ii.) In order to pause a container you will want to use the command: "podman pause (container_name). To resume use the command: "podman unpause (container_name)". 
    ii.) In order to restart you will want to use the command: "podman restart (container_name)".