pipeline {
    agent any
    
    stages {
        stage('List Running Containers') {
            steps {
                script {
                    // List running Docker containers
                    sh 'docker ps'
                    sh 'docker images'
                    sh 'docker ps -a'
                }
            }
        }
    }
}
