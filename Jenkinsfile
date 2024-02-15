pipeline {
    agent any
    
    stages {
        stage('Build') {
            steps {
                // Build your project here
                sh 'javac -d target src/Main.java'
                sh 'jar cf target/my_project.jar -C target/ .'
            }
        }
        
        stage('Archive Artifacts') {
            steps {
                // Archive the generated artifact
                archiveArtifacts artifacts: 'target/*.jar', fingerprint: true
            }
        }
    }
}
