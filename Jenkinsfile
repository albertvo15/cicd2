pipeline {
    agent any
    environment {
        BUILD_ID = 'v1.0.0'
    } 
    stages {
        stage('Build image') {
            steps {
                echo 'Starting to build docker image'

                script {
                    def customImage = docker.build("test:${env.BUILD_ID}")
                    customImage.push()
                }
            }
        }
    }
}
