pipeline {
    agent any
    // tools {
    //     maven 'Maven 3.9.9'
    //     jdk 'Java 17.0.12'
    // }
    stages {
        stage('Build') {
            steps {
                sh 'mvn clean package'
            }
            post {
                success {
                    echo 'Archiving...'
                    archiveArtifacts artifacts: '**/target/*.war'
                }
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploy step...'
            }
        }
    }
}
    


  
