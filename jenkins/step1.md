
### Create a folder where be files

`mkdir /root/jenkins`

### Run a instance of docker with jenkins installed

```
docker run -u 0 -p 8080:8080 -p 50000:50000 \
-v /root/jenkins:/var/jenkins_home \
-v /var/run/docker.sock:/var/run/docker.sock \
--name jenkins xlmriosx/jenkins:2.414.3-jdk17
```

> Maybe in the time you do this exists a new version of this image

#### [Now access Jenkins UI using this link]({{TRAFFIC_HOST1_8080}})

#### [Now access Jenkins where will be connected a slave agent]({{TRAFFIC_HOST1_50000}})

### Get password

`docker exec -it jenkins sh -c "cat /var/jenkins_home/secrets/initialAdminPassword"`

> The password is in /var/jenkins_home/secrets/initialAdminPassword

### Now we will install plugins

1. Go left panel, select "Manage Jenkins"
2. Go in "Stystem Configuration" select "Plugins"
3. Go left panel and select "Avaible plugins"
4. Search "docker" and select "Docker", "Docker pipeline"

### Later of install restart container with

`docker restart jenkins`

### Now to create some pipelines