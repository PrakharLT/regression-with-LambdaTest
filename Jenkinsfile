pipeline {
    agent any
    
     
    environment {
        // Append the paths to the directories containing Python and CMD executables
        PATH = "C:\\Python311;C:\\Windows\\System32;%PATH%"
    }
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
