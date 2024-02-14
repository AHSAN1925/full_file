pipeline {
    agent any
    
    environment {
        // Set Dockerfile location and image name
        DOCKERFILE_PATH = 'Dockerfile'
        IMAGE_NAME = 'my-docker-image'
    }
    
    stages {
        stage('Build Docker Image') {
            steps {
                script {
                    // Build Docker image using Dockerfile
                    docker.build IMAGE_NAME, "-f ${DOCKERFILE_PATH} ."
                }
            }
        }
    }
    
    stage('Run Container') {
            steps {
                // Run Docker container
                sh 'docker run -itd --name my-image my-docker-image'
            }
        }
}
