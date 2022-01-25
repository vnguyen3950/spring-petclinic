pipeline {
    agent any
    stages {

        stage('Maven package') {
            steps {
                sh './mvnw package'
            }
        }

        stage('Docker build') {
            steps {
                script{
                    dockerImage = docker.build petclinic
                }
            }
        }
    }
}
