pipeline {
    agent any
    
    stages {
        stage('Build') {
            steps {
                // Build your project here
                sh 'mvn clean package' // For Maven projects
                // Or: sh './gradlew build' // For Gradle projects
            }
        }
        
        stage('Archive Artifacts') {
            steps {
                // Archive the generated artifact
                archiveArtifacts artifacts: 'target/*.jar', fingerprint: true // For Maven projects
                // Or: archiveArtifacts artifacts: 'build/libs/*.jar', fingerprint: true // For Gradle projects
            }
        }
    }
}


