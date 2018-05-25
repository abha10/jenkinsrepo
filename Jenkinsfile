node {
    
    
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
          steps {
             echo "Deploying"
              def response = httpRequest 'https://dev39754.service-now.com/api/190726/snow_jenkins'
             println("Status: "+response.status)
              println("Content: "+response.content)
           }
        }
  
}
