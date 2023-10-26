
#### Step 1

Select in "Manage Jenkins" and "System"

<img style="margin-left: auto; margin-right: auto; width: 50%" src="../utils/assets/jenkins/step5/s5-1.png" style="width: 300px">

#### Step 2

Search "Global Pipeline Libraries", put name "`shared-library`" and set Default version like "`main`"

<img style="margin-left: auto; margin-right: auto; width: 50%" src="../utils/assets/jenkins/step5/s5-2.png" style="width: 300px">

#### Step 3

In "Source Code Managment" set "GitHub", paste in "Repository HTTPS URL" "`https://github.com/xlmriosx/jenkins-library.git`" and save

<img style="margin-left: auto; margin-right: auto; width: 50%" src="../utils/assets/jenkins/step5/s5-3.png" style="width: 300px">

#### Step 4

##### Option 1
Create a "Pipeline" and use:

```
@Library ('shared-library')_

pipeline {
    agent any
    stages{
        stage('Build'){
            steps{
                script{
                    build()
                }
            }
        }
    }
}
```

##### Option 2

Create a "Multibranch" and use previous repository (`https://github.com/xlmriosx/jenkins.git`)

Configurate "Script Path" like `shared-library/Jenkinsfile`
