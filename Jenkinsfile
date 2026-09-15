pipeline {
    agent any 
    parameters {
        string (name:'VERSION' defaultvalue: '1.0' description:'version to deploy')
        choice (name: 'ENVIRONMENT',choices: ['etaging,'production'],description: 'TARGET')
        booleanParam (name:'SKIP_TESTS',defaultValue: false, description: 'skip tests?")
                      }
    stages {
        stage('Build') {
            steps {
                echo 'Building'
            }
        }
    }
                      }
                                              
