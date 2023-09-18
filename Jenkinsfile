pipeline {
    agent any

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
                powershell """
                python test.py
                """
                
            }
        }
    }
}
