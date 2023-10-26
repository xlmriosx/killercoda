
## Slaves

> Documentation: https://www.jenkins.io/doc/book/scaling/architecting-for-scale/

### Local agent

For this we dont need configure

```
pipeline {
    agent any
    stages {
        stage('Test') {
            steps {
                echo "Hola mundo!"
                sh "java -version"
            }
        }
    }
}
```

### Server agent - Images agent

To do this we need to provision a server that contains what is needed to run the pipeline

1. Go left panel, select "Manage Jenkins"
2. Go in "Stystem Configuration" select "Nodes"
3. Set a name, select option of permanent agent and make configuration you need. Save agent configuration.
4. Search node and select command line you need and set run it in server with tools you need.

```
pipeline {
    agent { 
        label 'windows' /* In step 3, what you set in section "Label" is that you will specify here */
    }
    stages {
        stage('Test') {
            steps {
                powershell 'C:\\Actualizador.exe'
            }
        }
    }
}
```

### Ephemeral images agent

1. Install plugins before specified like "Docker" and "Docker pipeline"
2. Install docker where is running Jenkins
3. Specify in pipeline what image you need

To do this we need to specify an image that contains what is needed to run the pipeline

```
pipeline {
    agent {
        docker { image 'node:18.18.2-alpine3.18' }
    }
    stages {
        stage('Test') {
            steps {
                sh 'node --version'
            }
        }
    }
}
```
