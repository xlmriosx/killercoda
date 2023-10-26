
#### Step 1

Select in "New Item" 

<img style="margin-left: auto; margin-right: auto; width: 50%" src="../utils/assets/jenkins/step4/s4-1.png" style="width: 300px">

#### Step 2

Put a name, select "Multibranch" and click "Ok"

<img style="margin-left: auto; margin-right: auto; width: 50%" src="../utils/assets/jenkins/step4/s4-2.png" style="width: 300px">

#### Step 3

Go to "Branch Sources", select "GitHub" (`https://github.com/xlmriosx/jenkins.git`), and configure "Script Path" like above

<img style="margin-left: auto; margin-right: auto; width: 50%" src="../utils/assets/jenkins/step4/s4-3.png" style="width: 300px">

#### Step 4

To test differents pipeline try in Script Path:

- When: `when/Jenkinsfile`
- Parameters: `parameters/Jenkinsfile`
