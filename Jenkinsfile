stages {
        stage('Create Directory and File') {
            steps {
                script {
                    // Create a directory named 'my_directory'
                    sh 'mkdir my_directory'
                    
                    // Create a file named 'my_file.txt' inside the directory
                    sh 'touch my_directory/my_file.txt'
                    
                    // Write some data into the file
                    writeFile file: 'my_directory/my_file.txt', text: 'This is some data written into the file.'
                }
            }
        }
    }
