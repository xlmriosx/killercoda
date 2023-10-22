
### Create a simple pipeline with test-docker-slave

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