node {
    
    
        stage('Build') {
            
                echo 'Building..'
            
        }
        stage('Test') {
            
                echo 'Testing..'
            
        }
       stage('Deploy') {
          
             echo "Deploying"
              def response = httpRequest contentType: 'APPLICATION_JSON', httpMode: 'POST', ignoreSslErrors: true, responseHandle: 'NONE', url: 'https://dev39754.service-now.com/api/190726/snow_jenkins'
             println("Status: "+response.status)
              println("Content: "+response.content)
           }
        
  
}
