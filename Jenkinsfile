pipeline {
    agent any
    stages {
        
        stage("compile") {
            steps {
                bat 'javac Test.java'  // Use `bat` instead of `sh` for Windows
            }
        }

        stage("run") {
            steps {
                bat 'java Test'  // Use `bat` instead of `sh` for Windows
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
}
