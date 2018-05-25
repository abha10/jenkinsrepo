pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                echo 'Building..'
            }
        }
        stage('Test') {
            steps {
                echo 'Testing..'
            }
        }
       stage('Deploy') {
         lock('Deployment') {
         steps {
             echo "Deploying"
           }
        }
    }
  }
}
