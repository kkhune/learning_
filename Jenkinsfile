pipeline {
    agent any
    stages {
        stage('Checkout') {
            steps {
                // Checkout code from Git repository to a folder named 'source'
                checkout([$class: 'GitSCM', branches: [[name: '*/develop']], userRemoteConfigs: [[url: 'Your_Git_Repository_URL']]])
            }
        }
    }
}
wq!
q
q:
q!
