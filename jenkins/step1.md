
### Run a instance of docker with jenkins installed:

`docker run -p 8080:8080 -p 50000:50000 --name jenkins jenkins/jenkins:2.60.3`

### Now access Jenkins UI using this link:

[Jenkins UI]({{TRAFFIC_HOST1_8080}})

### Now access Jenkins where will be connected a slave agent:

[Jenkins slaves]({{TRAFFIC_HOST1_50000}})

