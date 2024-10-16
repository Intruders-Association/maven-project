pipeline {
  agent any  
  stages{
       stage ('Build'){
        steps {
          shell "mvn clean package"
          // sh 'mvn clean package'
        }
         post {
           success {
             echo 'Archiving...'
             archiveArtifacts '**/target/*.war'
           }
         }
       }       
       stage ('Deploy') {
        steps {
          echo 'Deploy step...' 
        }     
       }
  }
}  
// /target
  
