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
             archiveArtifacts artifacts:'**/target/*.war'
           }
         }
       }       
       stage ('Deploy to staging') {
        steps {
          build job 'deploy-to-staging' 
        }     
       }
  }
}  
// /target
  
