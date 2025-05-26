@Library('my-shared-lib') _
import org.iti.DockerShared1

node('Agent1') {
    def docker = new DockerShared1(this)
    withCredentials([usernamePassword(
        credentialsId: 'docker-hub-creds',
        usernameVariable: 'USERNAME',
        passwordVariable: 'PASSWD'
    )]) {
        stage("Login Docker Hub") {
            docker.login(USERNAME, PASSWD)
        }
    }

    stage("Build Docker Image") {
        docker.buildPythonImage()
    }

    stage("Push Docker Image") {
        docker.pushPythonImage()
    }
}
