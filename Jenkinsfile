pipeline {
    agent any
    
    environment {
        DOCKER_IMAGE = 'nginx:latest'
        CONTAINER_NAME = 'my-nginx-container12'
        PORT = 8080
    }
    
    stages {
        stage('Build Docker Image') {
            steps {
                script {
                    docker.build DOCKER_IMAGE, '.'
                }
            }
        }
        
        stage('Run Docker Container') {
            steps {
                script {
                    // Run Docker container from the built image
                    def container = docker.image(DOCKER_IMAGE).run('-d -p ${PORT}:80 --name ${CONTAINER_NAME}')
                    
                    // Show the logs of the running container
                    container.inside {
                        sh 'echo "Container is running..."'
                        sh 'echo "Container ID: $(hostname)"'
                    }
                }
            }
        }
    }
}
