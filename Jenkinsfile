pipeline {
  agent any  
  stages{
       stage ('Build'){
        steps {
          cygwin "mvn clean package"
          // sh 'mvn clean package'
        }
         post {
           success {
             echo 'Archiving...'
             archiveArtifacts artifacts:'**/target/*.war'
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
  
