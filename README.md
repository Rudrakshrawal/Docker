# Docker


-------------------------------
# Setting environment

## Install docker on OS
https://hub.docker.com

------
--------
# [DockerOfficial](https://www.docker.com/products/docker-desktop/)
Download the app of docker from the official site. After that you have many **Linux Distributors or Distros**(variations of the Linux operating system that are built using the Linux kernel along with various software packages and components):
  
  - Ubuntu
  - Debian
  - Alpine
  - Fidora
  - And many thousand more

After this you can run these Open source operating systems on your device.

-----------------
## To Dockerize your files:
_Assume we are creating an app_
- <img width="1114" alt="image" src="https://github.com/Rudrakshrawal/Docker/assets/144530387/3b3543d6-e374-45cb-b074-94b637f6ec19">

### Instructions:
- Start with an os
- Install node
- Copy app file
- Run the file using node.js

### For this:
we will create a folder along with the app file with the name ```Dockerfile```. You can/should also download the docker extension in your IDE (in this case vs code)



<img width="1114" alt="image" src="https://github.com/Rudrakshrawal/Docker/assets/144530387/42ac3166-8a44-460c-a3fa-a33e4a473d51">




### Writing the contents in the file
<img width="755" alt="image" src="https://github.com/Rudrakshrawal/Docker/assets/144530387/2eb29685-372d-410b-a1fa-f5a2fc6c5eff">


- The ```FROM``` is the base image which contains various files in it and we will/can also add adiitional files in it, like inheritance in programming. Now we could've installed the linux image with node on top of it, but here we are using node image which is already build on top of linux . These images are already published on the [DockerHub](https://hub.docker.com/). Here we specified the tag using a : to specify which linux distribution system we wanna use. Here we are using alpine.
- In the ```COPY  ``` command we are gonna copy all the files in the current directory into the app directory into that image.
- By adding the ```WORKDIR``` command we can specify the current working directory
- The ```CMD``` command will be used to execute what actions or command do we need to perform.


------------------------

## Creating an image
- change the directory to where all the files are.
- By going to the terminal and running the command:
  ```
  docker build -t hello-docker .
  ```  
- Here we are creating an image with the tag(-t) hello-docker with the location of the current directory ( . )
- We can see our docker image using thee command ```docker image ls```
- now when we run the iamge ```docker run hello-world``` the file will show the output "Hello world!"



## Now deploying the image
- first to deploy the image you will have to create a dockerhub account
- then log into the account using ```docker login``` on your terminal
- ```docker push your_repository_name:tag``` : Using this command we can push our image to the DockerHub


-----------------

## Steps to launch an image on your machine
- Go to the official docker app to check for these Distros and how to pull them
- In this case we'll use ubuntu. For that run the command ```docker pull ubuntu``` this will pull the image for ubuntu. But you can also run the command ```docker run ubuntu``` which will pull ubuntu in background .
- You can use the ``` docker ps``` commannd to check the images running and ``` docker ps-a ``` to check all the images running on the docker
- To start using ubuntu you will run the command ```docker run -it ubuntu``` , this will start the ubuntu os on your device by opening a shell which will pass the instructions to the OS, just like a terminal or cmd prompt. ```root@db8d19b4728f:/#``` something like this will open, lets break it down. _root_: currently logged in user, in this case a root user who has the highest privellages.      _b8d19b4728f_: The name of the machine       _/#_: represents the folder directory, the highest directory in the system. If you would have accessed it as a root user you would've had the $ sign
- you can run different commands.   ```echo hello``` :prints hello    ```whoami``` :prints hello
- ```echo $0``` : will show the location of the shell program   .The  output ```/bin/bash``` means a directory named bin in which there is bash (short for Born Again Shell)
- ```history``` will show the history of the commands
- ```apt ``` apt: advanced packaged tool
- ```nano``` nano:basic text editor for linux
- ```apt list``` will show the list of all the packages that can be installed
- ```apt install nano``` will show an error, this occurs because the ```apt``` command does not contain all the packages in it, for that we'll need to run the command ```apt update``` through which linux is going to download all the list of packages
- The package is successfully installed but to check we'll run the command ```nano```. to exit you can press **command + x**
- You can clear the terminal by **control + l**
- You can remove it too using ```apt remove nano```
  
------------- 

## What are the files in this linux system ??
/         (Root Directory)
- bin: includes binaries/ programs
- boot: files related to booting
- dev: (devices) 
- etc: (editable text configuration) Contains system-wide configuration files.
- home: user home directories
- root: home directory for the root user
- lib: contains shared library files
- var: Contains variable data files, such as logs and temporary files.
- proc: Provides information about processes and system resources as files and directories.
**EVERYTHING IS A FILE IN LINUX**

-----------------
## Navigating the file system
- ```pwd``` : short for print working directory
- ```ls``` : to see the list of files/directories
-  ```cd``` : to change directory(folder).  While writing the name ```TAB``` button can be pressed to autofill
-   ```cd ..```: to go just one directory back
-   ```cd ~```: to go to root directory
-   ```mkdir file_name```: will create a new file
-   ```mv```: to rename or move the file
-   ```touch ``` : to create a writable file such as txt or python. Many files can also be created at once
-   ```rm```: to remove one or multiple files at once
-   ```rm -r```: to remove a whole directory. r means recurrsive
-   ```nano```: text editor for linux, You may have to first install it
-   ```cat```: to view the contents of the file. Using ```cat file1.txt > file2.txt``` we can concatenate the contents of the content into file2.txt
-   ```more``` : to view the content percentage wise. go down
-   ```less```: to go up
-   ```head -n 5```: to see the first 5 lines of the file
-   ```tail -n 5```: to see the last 5 lines of the file
-   



-------
