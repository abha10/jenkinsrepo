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
             //def response = httpRequest consoleLogResponseBody: true, contentType: 'APPLICATION_JSON', httpMode: 'POST', ignoreSslErrors: true, requestBody: '{"status":"failure","request-item-id":"${params.Request-Item-ID}"}', url: 'https://dev39754.service-now.com/api/190726/snow_jenkins'
           echo "${params.Request_Item_Number}";
           echo "${params.status}";
           echo "${params.job_name}";
       //    var jobBuild =  "${params.job_name}";
         //  echo jobBuild.getResult()
           echo "${params.build_number}";
         //  def response = httpRequest consoleLogResponseBody: true, contentType: 'APPLICATION_JSON', httpMode: 'POST', ignoreSslErrors: true, requestBody:"${params.Request_Item_Number}", url: 'https://dev39754.service-now.com/api/190726/snow_jenkins'  
           //   def response = httpRequest consoleLogResponseBody: true, contentType: 'APPLICATION_JSON', httpMode: 'POST', ignoreSslErrors: true, url: 'https://dev39754.service-now.com/api/190726/snow_jenkins?status=${BUILD_STATUS}&request_item_number=${params.Request_Item_Number}&job_name=${JOB_NAME}&build_number=${BUILD_NUMBER}'  
           def response = httpRequest consoleLogResponseBody: true, contentType: 'APPLICATION_JSON', httpMode: 'POST', ignoreSslErrors: true, url: 'https://dev39754.service-now.com/api/190726/snow_jenkins'
           //println("Status: "+response.status)
  //            println("Content: "+response.content)
             try {
        // do something that fails
        sh "exit 1"
        currentBuild.result = 'SUCCESS'
    } catch (Exception err) {
        currentBuild.result = 'FAILURE'
    }
    echo "RESULT: ${currentBuild.result}"
           
           }
        
  
}
