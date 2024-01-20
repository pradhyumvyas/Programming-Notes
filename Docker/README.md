# Docker

### Problem statement which docker is solving
   1) Same environment replica
      - Provide same environmet for each and every services and bind them in one container.
      - To run a project in a very large scale team size it is getting very hard to setup same environment across all team member machines in different OS's also, with the help of Docker we can easily overcome this issue.
      - Some services are OS specifics like some service wil run in windows machines only but we needed same in MacOS also, by the help of Docker we can acheive this also.
   2) Setup environment in cloud for every instance
      - It is getting very tough to setup same environment to deploy our services on cloud
      - If we are using serverless then in each and every instance we have to replicate same environment
      - We can solve this problem with the help of Docker.

### Docker Container
   1) Container
      - Inside container we will create all our services and install all our required software or packages.
      - like we can create **Container** with below services
         - OS:Linux
         - Tools: Node, MongoDB, ReactJS, SQL and many more
      - And we can use this container anywhere by running our Docker container
   2) Installation of Docekr CLI and Desktop
      - Download [Docker](https://www.docker.com/products/docker-desktop/) and install
      - It will download docker and provide **Daemon** and **Docker Desktop**
      - To run Ubuntu container in our machine run this command for running ubunut in container
      - ```docker run -it ubuntu ```
      - it will install ubuntu image in you local docker container, after installing it will available in Docker desktop
      - it will download from [hub.docker.com](https://hub.docker.com)
      - It will provide a isolate container, where we can download and run anything it will not affect our physical machine.
      - **Docker images behave like a OS and container run this images which are isolated from each container, can be created multiple container with single image**

   3) Port Mapping
      - As Docker container is Isolated from our physical machine so it will not be accessible from physical machine browser
      - let say node env is running in PORT:8000, so it will not be available in chrome browser, it will throw not found error.
      - So for solving this we can expose container PORT
      - To expose have to run below command in physical machine terminal
      - ```docker run -it -p <physical_machine_port>:<container_port> <image_name>```
   4) Environment variable
      - We can pass env variable also when we are running image in host server
      - ```docker run -it -p <physical_machine_port>:<container_port> -e key=value -e key=value <image_name>```
   
   5) Dockerization 
      - Dockerize node js server
         - create one file with name **Dockerfile** without any extension
         - check all config in Dockerfile from above dir
         - after adding configuration build the docker image from below command
         - ``` docker build -t <our_image_name> <docker_file path '.'>```
         - -t means tag, in <docker_file_path> press **dot(.)** if it in parent dir
         - After building it will availbale in Image section of Docker Desktop
         - after running and mapping port, we will be able to run in out host machine
      - Caching the layer
         - Every command in Dockerfile it is in cache, so add command according to it 
      - Publish to Docker Hub
         - Create accoung on docker hub and create image from portal
         - build our docker image with the same name as we created on docker portal
         - And Run below command
         - ``` docker push <image_name>```
         - If it is throwing error 'denied:requested access to the resource is denied' error, then we have to login, for login run below command
         - ```docker login``` and provide credentials
         - after login push docker image, it will available in docker hub portal after push 
   6) Docker Compose
      - Services
         - Sometimes we have to use multiple container or images for running a project
         - One way is we can run each caontainer command one by one and use it, but it will not preferable
         - (Preferred way): create **docker-compose.yml** file and add config file inside this, we can setup, create and destroy container from this
         - Check the above ***docker-compose.yml*** file
         - After adding config run below command
         - ```sudo docker compose up```
         - It will up and running all the services which are in compose file
         - It will create node and run all container inside this one, it can be available in Docker Desktop
         - to stop compose service run below command
         - ```sudo docker compose down```
      - Port Mapping
      - Env Variable


### Docker Commands
   - ```docker run -it <image_name> ``` --> It will pull docker image from docker hub repo
   - ```docker container ls ```  --> Display running container
   - ```docker container ls -a```  --> Display all container
   - ```docker start <contaienr_name> ```
   - ```docker stop <contaienr_name> ```
   - ```docker exec <contaienr_name> ls``` --> Just for dispaly dir in container
   - ```docker exec -it <contaienr_name> bash``` --> attach terminal in container
   - ```docker images ```


      
