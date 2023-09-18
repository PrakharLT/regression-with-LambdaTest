pipeline {
    agent any
    
     environment {
        // Add the path to Python executable
        PATH = "C:\\Python311;$PATH"
        // Add the path to cmd
        PATH = "C:\\Windows\\System32;$PATH"
    
    stages {
        stage('Checkout') {
            steps {
                // Checkout the Git repository with the correct default branch
                checkout([$class: 'GitSCM', branches: [[name: 'main']], userRemoteConfigs: [[url: 'https://github.com/PrakharLT/regression-with-LambdaTest.git']]])
            }
        }

        stage('Run Python Script') {
            steps {
                // Run the Python script using the Python executable
                
                bat 'python3 test.py'
                
                
            }
        }
    }
}
