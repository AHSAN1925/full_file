pipeline {
    agent any
    
    stages {
        stage('Build') {
            steps {
                // Build your project here
                sh 'mvn clean package'
            }
        }
        
        stage('Archive Artifacts') {
            steps {
                // Archive the generated artifact
                archiveArtifacts artifacts: 'target/*.jar', fingerprint: true
                // Archive any other required files
                archiveArtifacts artifacts: 'docs/*.pdf', fingerprint: true
                archiveArtifacts artifacts: 'config/*.xml', fingerprint: true
            }
        }
    }
}
