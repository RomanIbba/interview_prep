
# Getting Started

    -Make sure docker is installed then in terminal run

`docker pull ubuntu` (ubuntu can be replaced with other images from hub.docker)

    -First will look on local for Ubuntu, if not there it will pull from hub.docker
    -Next execute the image by creating a container

`docker run -it ubuntu` (it stands for interactive)

    -The terminal will look exactly like the Ubuntu command line
    -Try: ls -> cd home/ -> mkdir hello -> touch hello-ubuntu.txt -> ls
    -You just made a .txt file using Ubuntu
    -You are running an entirely different operating system simply by executing a docker image with a container
    -Kill terminal by clicking the trash button on the upper right if using VS code

