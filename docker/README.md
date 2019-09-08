# What is docker?
 Docker is containerization tool for running applications,
 Today docker is widely used for running apps, and lots of migrations from VM to containers is happening in the industry
 
# Why we shoud use docker?
  - Docker containers are light weight i.e. they consume fewer resources, docker containers stats in 1-2 seconds
  - Docker is higly portable
  - Docker apps will scale better than VM based apps
  - Deploying docker apps is easy and fast (most important for micro services based applications)
  
 # The process of dockerizing application
 
 ```
    Write Dockerfile --> Build Docker Image --> Create Docker Container
 ```
 
 # Run Docker Container on VM
 
  - take virtual machine (EC2 from AWS)
  - Install docker daemon on EC2
    ```
      sudo yum install docker -y
      sudo chkconfig docker on
      sudo service docker start
    ```

## Run tomcat in docker container

```
  sudo docker run -d --rm -p 8080:8080 tomcat:8.0
```
``` -d ``` stands for detach mode, you container runs in detach mode
``` -it ``` stands for interactive terminal i.e. you container runs in fore ground
``` -p ``` port mapping, this maps a port on a vm with port on a docker containr

## Access tomcat
```
  http://docker-host-ip:8080
```

## Addiing custom user to docker group
Such that we do not have to put sudo in front of every docker command.

```
  sudo usermod -a -G docker ec2-user
  sudo service docker restart
  Relogin to VM
```
