pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                checkout([
                    $class: 'GitSCM',
                    branches: [[name: '*/main']],
                    userRemoteConfigs: [[url: 'https://github.com/salunkenikita2206-jpg/gha-assignment.git']],
                    extensions: [
                        [$class: 'CleanBeforeCheckout'],
                        [$class: 'WipeWorkspace']
                    ]
                ])
            }
        }
    }
}
