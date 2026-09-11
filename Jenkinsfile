pipeline {
    agent any

    environment {
        APP_ENV = 'staging'
    }

    stages {
        stage('Build') {
            steps {
                retry(3) {
                    sh 'echo "Building application in environment: ${APP_ENV}..."'
                }
            }
        }
        stage('Test') {
            steps {
                script {
                    try {
                        sh 'echo "Running tests..."'
                    } catch (err) {
                        currentBuild.result = 'UNSTABLE'
                    }
                }
            }
        }
    }
}
