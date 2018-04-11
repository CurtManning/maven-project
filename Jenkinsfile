pipeline {
    agent any
    stages{
        stage('Build'){
            steps {
                bat 'mvn clean pipeline-package'
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