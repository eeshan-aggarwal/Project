pipeline {
    agent any
    environment {
        VERSION_NAME = "1.34"  // Environment variable
    }
    stages {
        
        stage("compile") {
            steps {
                bat 'javac Test.java'
                bat 'echo %VERSION_NAME%'  // Correct Windows syntax for environment variable
            }
        }

        stage("run") {
            steps {
                bat 'java Test'  // Use `bat` instead of `sh` for Windows
            }
        }
    }
    post {
        always {
            bat 'echo "always"'  // Use `bat` for Windows commands
        }
        success {
            bat 'echo "success"'  // Use `bat` for Windows commands
        }
        failure {
            bat 'echo "failure"'  // Use `bat` for Windows commands
        }
    }
}
