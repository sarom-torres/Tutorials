# Architecture 
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

-------------------------
## Dockerfile

### ARG vs ENV

`ARG` 
- Defines a variable that users can pass at build-time to the builder. 
- They are only available from the moment they are ‘announced’ in the Dockerfile with an ARG instruction up to the moment when the image is built. 
- Running containers can’t access values of ARG variables. 
- This also applies to `CMD` and `ENTRYPOINT` instructions which just tell what the container should run by default. 
- If you tell a Dockerfile to expect various ARG variables (without a default value) but none are provided when running the build command, there will be an error message.

`ENV` 

- Environment variables are also available during the build, however they are also accessible by containers started from the final image.
- Environment variables are notated in the Dockerfile either with `$variable_name` or `${variable_name}`

![image](https://user-images.githubusercontent.com/34520860/116629790-69939e00-a928-11eb-8180-bdfcd8bd645f.png)
