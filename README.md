# Jira Workshop: Installing and setting up Jira

## Prerequisites
To be able to run Docker you need a x64 architecture (64 bits). If you don't have 64 bits system and 64 bits OS, you can install Jira [manually](MANUAL.md). On Windows (and possible other platforms) you need to [enable virtualisation](http://www.howtogeek.com/213795/how-to-enable-intel-vt-x-in-your-computers-bios-or-uefi-firmware/) (VT-X/AMD-V) and disable Hyper-V on Windows. 

## Info
Provides info and scripts for creating a Docker environment with Jira running for Workshop purposes. Main source for this script is https://cptactionhank.github.io/docker-atlassian-jira/. The following setup needs about 30 minutes from your time and about 1Gb diskspace. This setup needs less manual intervention than the [manual](MANUAL.md) setup.

## Script
1. Install the [Docker Toolbox](https://www.docker.com/products/docker-toolbox)
2. Docker comes with Kitematic. Start the Kitematic app, it will create a docker-machine with the name 'default'. From now on you can create and run docker images. When Kinematic fails to start you can try to start a docker-machine yourself in a terminal/cmd-window: ```docker-machine.exe create -d virtualbox default```. For windows you might have to go to ```C:\Program Files\Docker Toolbox``` first, before running the docker-machine command. 
3. Minimize the Kitematic app and let it run as a background process.
4. For Linux/Mac: Open a terminal/cmd-window and run the command ```docker-machine env```. Check to see if the docker-machine has a valid name (DOCKER_MACHINE_NAME) and ip-address (DOCKER_HOST). Now run ```eval $(docker-machine env)```. 
5. For Windows: Open a terminal/cmd-window and run the command ```docker-machine.exe env default```. Check to see if the docker-machine has a valid name (DOCKER_MACHINE_NAME) and ip-address (DOCKER_HOST). Now run ``` FOR /f "tokens=*" %i IN ('docker-machine.exe env default') DO %i```. 
6. Make sure you don't have any processes running that can occupy the port 8080 (or use a custom port after the colon in the following command). Open a terminal/cmd-window and :

  ```docker run --detach --publish 8080:8080 cptactionhank/atlassian-jira:6.3.10```.

  This command will download an run a Linux-image with Jira pre-installed and running.

7. After downloading for 5-10 minutes your Jira-application is available on DOCKER_MACHINE_NAME:8080. The docker-machine fill forward the 8080 port to the docker-image that's running Jira. This docker-image has a private ip-address, but we don't need to connect to this specific machine.

8. Visit http://DOCKER_MACHINE_NAME:8080 in your browser. The Jira configuration-screen will open. Choose: "Set it up for me", this option is enough for setting up an evaluation or demonstration environment. Choose Next, Jira will setup an in-memory database in a few minutes.

9. Almost done. Pick "Software development*" and choose Next. Create a [My Atlassian Account](https://my.atlassian.com) and generate an evaluation license for Jira. Install the license and create an administrator account.

10. Create a new Scrum-board with Board name and Project name "Workshop", Jira will generate a project key "WOR", that's OK. Select "Agile simplified workflow" and click "Create board".

11. You're ready for the Workshop! When you're done with the workshop you can list the current running images with ```docker ps``` and stop the docker-image with the command ```docker stop <imagename>``` and close the Kitematic app.
