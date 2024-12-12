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
    }
}
