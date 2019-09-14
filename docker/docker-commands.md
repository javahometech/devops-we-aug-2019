## Docker Commands
- docker info
- docker images
    ``` Display all images on current docker host ```
- docker rmi image-id
   ```Remove specific image```
- docker rmi $(docker images -q)
    ```Remove all images```
- docker images prune
    ```Remove all unused images```
- docker build -t kammana/atm:1.0 .
    ```Build docker image```
- docker tag old-image  new-image
    ```Changing the tag of existing image```
- docker login -u user-name -p password
    ```Login to Docker hub```
- docker push kammana/atm:1.0
    ```Pushing images to docker hub```
- docker pull kammana/atm:1.0
    ```Pull docker images ```
- docker run -d -p 8080:5000 --name=myapp kammana/online-app:1.0

  ```
    -d stands for detached, i.e. run containers in background
    -it stands for interactive terminal which runs containers in foreground
    -p stands for port maping host-port:container-port
    
    --rm remove the container when container exits/stops
    
    --name for giving your own friendly name to containers, if not menstioned docker picks random name
  
  ```
 
 - docker ps show containers in running state
 - docker ps -a show containers in running and exited status
 - docker ps -aq show only container ids 
 - docker start container-id/name
 - docker stop container-id/name
 - docker restart container-id/name
 - docker rm container-id/name  remove container
 - docker rm -f container-id/name  remove container force remove
 - docker rm $(docker ps -aq)
