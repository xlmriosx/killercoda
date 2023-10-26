
#### Step 1

Select in "New Item" 

<img style="margin-left: auto; margin-right: auto; width: 50%" src="../utils/assets/jenkins/step3/s3-1.png" style="width: 300px">

#### Step 2

Put a name, select "Pipeline" and click "Ok"

<img style="margin-left: auto; margin-right: auto; width: 50%" src="../utils/assets/jenkins/step3/s3-2.png" style="width: 300px">

#### Step 3

Go to "Advanced Project Options", select "Pipeline script", and configure script like above

<img style="margin-left: auto; margin-right: auto; width: 50%" src="../utils/assets/jenkins/step3/s3-3.png" style="width: 300px">

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
