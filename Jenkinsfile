node('Agent1'){


        stage("build Docker image"){
            
                sh "docker build -t faresayyman/data-iti:v${BUILD_NUMBER} ."
            }
        
        stage("Push Docker image"){
          
                sh "docker push faresayyman/data-iti:v${BUILD_NUMBER}"
            
        }
    }
