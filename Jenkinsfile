node {
    
    
        stage('Build') {
            
                echo 'Building..'
            
        }
        stage('Test') {
            
                echo 'Testing..'
            
        }
       stage('Deploy') {
          
             echo "Deploying"
              //def response = httpRequest consoleLogResponseBody: true, contentType: 'APPLICATION_JSON', httpMode: 'POST', ignoreSslErrors: true, url: 'https://dev39754.service-now.com/api/190726/snow_jenkins'
             def response = httpRequest consoleLogResponseBody: true, contentType: 'APPLICATION_JSON', httpMode: 'POST', ignoreSslErrors: true, requestBody: '{"status":"failure","request-item-id":"${params.Request-Item-ID}"}', url: 'https://dev39754.service-now.com/api/190726/snow_jenkins'
//             println("Status: "+response.status)
  //            println("Content: "+response.content)
           }
        
  
}
