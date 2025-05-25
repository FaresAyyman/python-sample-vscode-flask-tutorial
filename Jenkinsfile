pipeline{
    agent{
        label "agent1"
    }

    stages{
        stage("build Docker image"){
            steps{
                sh "docker build -t faresayyman/data-iti:v${BUILD_NUMBER} ."
            }
        }
        stage("Push Docker image"){
            steps{
                sh "docker push faresayyman/data-iti:v${BUILD_NUMBER}"
            }
        }
    }
}
