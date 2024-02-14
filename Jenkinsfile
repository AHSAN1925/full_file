pipeline {
    agent any
    
    stages {
        stage('Build') {
            steps {
                // Checkout the Git repository
                git 'https://github.com/username/repository.git'
                
                // Build the Maven project
                sh 'mvn clean package'
            }
        }
        
        stage('Archive Artifacts') {
            steps {
                // Archive the generated JAR file as an artifact
                archiveArtifacts artifacts: '**/target/*.jar', fingerprint: true
            }
        }
    }
}
