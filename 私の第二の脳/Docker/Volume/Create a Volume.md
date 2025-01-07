```bash
#Create a volume
docker volume create myvol

#Inspect the volume
docker volume inspect myvol

#List the volumes
docker volume ls 

#Run a container with a volume
docker run -d --name devtest -v myvol:/app nginx:latest
```
## Tags

###### #Docker