# Docker

## Overview
*Image*: Executable package, contains code, runtime, libraries, environment variables, config files  
*Container*: Launched by running image, runtime instance of an image

## Define container 
### Required Files
- Dockerfile  
- requirements.txt  
- app.py  

### Build
Build a container with a `imagename` and `tag` (e.g. v0.1):  
```bash
docker build --tag=imagename:v0.1
```
Shows all images:  
```bash
docker image ls
```

### Run app
```bash
docker run -p 4000:80 imagename
```
Shows all running containers:  
```bash
docker container ls
```

### Tag image, publish and pull & run from remote repository
Tag image:  
```bash
docker tag imagename username/repository-name:tag
```
Publish:  
```bash
docker push username/repository-name:tag
```
Pull & run from remote repository:  
```bash
docker run -p 4000:80 username/repository-name:tag
```

