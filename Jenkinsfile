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
                    def dockerImage = docker.build("petclinic:${env.BUILD_ID}")
                }
            }
        }
    }
}
