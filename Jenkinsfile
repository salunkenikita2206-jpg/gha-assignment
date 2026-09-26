pipeline {
    agent any 
    stages {
        stage('hello') {
            steps {
                echo 'This just prints a message'
                sh 'echo this runs a real shell command'
                sh 'pwd'
                sh 'ls -la'
            }
