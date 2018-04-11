pipeline {
    agent any
    stages{
        stage('Build'){
            steps {
                echo 'Hello...'
            }
            post {
                success {
                    echo 'Now Archiving...'
                    archiveArtifacts artifacts: '**/target/*.war'
                }
            }
        }
    }
}