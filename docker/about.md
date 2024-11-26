
## What is Docker?
-	Makes sure applications run smoothly in any environment without surprises
-	Enables the development, packaging and execution of applications in a unified environment
-	By clearly specifying application requirements such as node.js versions and packages docker generates a self contained box that includes its own operating system and all the components essential for running an application

## Why use Docker?
-	Big companies noticed that using docker made their apps better and faster in development and deployment
-	Onboarding new developers took days instead of weeks
-	Everyone uses the same commands to run the app no matter what computer they are using
-	Portability, easily move application between different stages: development, testing and production
-	Helps with version control, tracks versions of application. Can revert to previous version if something goes wrong
-	Scalability, creates copies of the application when needed
-	Dev ops integration, ensures application is developed, tested and deployed efficiently

## How does Docker work?
-	Two most important concepts- images and containers
-	Images- lightweight, standalone, executable package that includes everything needed to run a piece of software including the code, runtimes like node.js, libraries, system tools and even the operating system
-	Think of docker image as a recipe for our application, ingredients = code and libraries, recipe = runtime and system tools
-	Container- a runnable instance of a docker image. Execution environment for application. Takes everything in the image and follows its instructions by executing necessary commands, downloading packages and setting things up to run application
-	Symbolism: a baked cake is the container, it is the end result of following the image recipe
-	Can run multiple containers for a single image, create one image and get as many instances as we want from it
-	Volume- persistent data storage mechanism that allows data to be shared between a docker container and a host machine. Ensures data durability and persistence
-	Network- a channel that allows different containers to communicate with each other or with the external world

## Docker workflow
-	Docker client, docker host (docker daemon) and docker registry (docker hub)
-	Docker client- user interface for interacting with docker, tool we use to give docker commands (command line, UI, etc) instructing it to build, run or manage images or containers. Think of it as the chef giving instructions to kitchen staff
-	Docker host- background process for managing containers on the host system
-	Docker registry- centralized repository of docker images, hosts both public and private repositories. Docker hub is to docker as GitHub is to git

## How to use Docker
-	Docker.desktop and hub.docker.com
-	All starts at the dockerfile, a set of instructions telling docker how to build an image for your application
-	Keywords/ commands
-	FROM-> specifies the base image to use for the new image
-	WORKDIR-> sets the working directory for the following instructions (where in the kitchen to do your cooking)
-	COPY-> copies the files or directories from the build context to the image (bringing ingredients/ tools to cooking spot)
-	RUN-> executes commands in the shell during image build (doing specific steps such as mixing ingredients)
-	EXPOZE-> informs docker that the container will listen on specified network ports on runtime
-	ENV-> sets environment variables during the build process
-	ARG-> decides the build time variables
-	VOLUME-> creates a mount point for externally mounted volumes. Specifying a location inside your container where you can connect external storage
-	CMD-> provides default command to execute when the container starts
-	ENTRYPOINT-> setting a fixed starting point for your container

