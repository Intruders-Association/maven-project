pipeline {
  agent any  
  stages{
       stage ('Build'){
        steps {
          sh 'mvn clean package'
        }
         post {
           success {
             echo 'Archiving...'
             archiveArtifacts artifacts:'**/target/*.war'
           }
         }
       }
       stage ('Build') {
        steps {
          echo 'Build step...'
        }
       }
       stage ('Deploy to prod') {
        steps {
          echo 'Deploy step...' 
        }     
       }
  }
}    
  
