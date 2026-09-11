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
                sh 'echo "Building application..."'
            }
        }
        stage('Test') {
            steps {
                sh 'echo "Running test suite..."'
            }
        }
        stage('Deploy') {
            when {
                branch 'main'
            }
            steps {
                sh 'echo "Deploying application..."'
            }
        }
    }

    post {
        always {
            archiveArtifacts artifacts: 'test-reports/**', allowEmptyArchive: true
        }
        success {
            echo 'Pipeline succeeded'
        }
        failure {
            echo 'Pipeline failed'
        }
    }
}
