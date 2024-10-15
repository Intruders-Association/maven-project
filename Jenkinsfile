pipeline {
  agent any  
  stages{
       stage ('Build'){
        steps {
          echo 'Build...'
          sh 'mvn clean package'
        }
         post {
           success {
             echo 'Archiving...'
             archiveArtifacts artifacts:'**/target/*.war'
           }
         }
       }       
       stage ('Deploy to prod') {
        steps {
          echo 'Deploy step...' 
        }     
       }
  }
}    
  
