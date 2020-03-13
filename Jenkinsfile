pipeline{

    agent any

    stages{

        stage('Build'){

            steps{

                sh 'mvn clean package'
            }    

            post {

                sucsess {

                    echo "Now archiving..."
                    archieveArtifacts artifacts: '**/*.war'
                }
            }
        }
    }
}
