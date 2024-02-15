pipeline {
    agent any
    
    stages {
        stage('Build') {
            steps {
                script {
                    // Print current directory
                    sh 'pwd'
                    // List contents of src directory
                    sh 'ls -l src'
                    // Compile Java file
                    sh 'javac -d target src/Main.java'
                }
            }
        }
    }
}

