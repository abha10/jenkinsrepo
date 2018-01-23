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
         input "Deploy?"
         milestone()
         lock('Deployment') {
         steps {
             echo "Deploying"
           }
        }
    }
	}
}
