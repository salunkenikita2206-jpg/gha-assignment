pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                checkout scm
            }
        }
        stage('Build') {
            steps {
                sh 'echo "Installing dependencies..."'
                sh 'echo "Building project..."'
            }
        }
        stage('Parallel Tests') {
            parallel {
                stage('Unit Tests') {
                    steps {
                        sh 'echo "Running unit tests..."'
                    }
                }
                stage('Lint') {
                    steps {
                        sh 'echo "Running linter..."'
                    }
                }
            }
        }
    }

    post {
        always {
            cleanWs()
        }
    }
}
