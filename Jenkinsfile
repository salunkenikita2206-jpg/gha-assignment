pipeline {
    agent any 
   parameters {
       choice(name: 'ENVIRONMENT',choices: ['staging','production'],description: 'Target')
   }
   stages {
           stage('Tests') {
             stage('Approve') {
                   steps {
                       input message: 'Deploy to production ?'
               parallel {
                   stage('Unit') { steps { sh 'echo Unit tests' } }
                   stage('Integration') { steps { sh 'echo Integration tests' } }
               post {
                   success {
                       echo 'Pipeline suceeded'
                   }
                   failure {
                       echo 'Pipeline failed'
                   }
               }
           }
       }
   }
}

    
