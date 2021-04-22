## Architecture
![arch-docker](https://user-images.githubusercontent.com/34520860/115405975-1cdff280-a1c5-11eb-8e6a-ae047fd7139d.png)

## Basic commands 

### Fetche the image from the docker Registry and save on host system.
```
docker pull [image-name]
```
### List all images on the host system
```
docker images
```
### Run an docker image
```
docker run [image-name]
```
### Show all containers that are currently running
```
docker ps -a
```
### Remove an docker image
```
docker rmi [image-name-or-id]
```
or
```
docker image rm [image-name-or-id]
```
