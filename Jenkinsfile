pipeline {
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
