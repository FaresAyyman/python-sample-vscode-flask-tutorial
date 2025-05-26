@Library('my-shared-lib') _

node('Agent1') {
    withCredentials([usernamePassword(
        credentialsId: 'docker-hub-creds',
        usernameVariable: 'USERNAME',
        passwordVariable: 'PASSWD'
    )]) {
        stage("Login Docker Hub") {
            DockerShared1.login(USERNAME, PASSWD)
        }
    }

    stage("Build Docker Image") {
        DockerShared1.buildPythonImage()
    }

    stage("Push Docker Image") {
        DockerShared1.pushPythonImage()
    }
}
