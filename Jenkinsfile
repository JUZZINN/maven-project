pipeline {
    environment {
    registry = "docker_hub_account/repository_name"
    registryCredential = 'dockerhub'

    agent any
    stages{
        stage('Build'){
            steps{
                sh 'mvn clean package'
                sh "docker build . -t tomcattwebapp:${env.BUILD_ID}"
            }
        }
    }
    }
}
