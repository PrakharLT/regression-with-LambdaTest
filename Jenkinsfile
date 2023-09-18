pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                // Checkout the Git repository
                checkout scm
            }
        }

        stage('Run Python Script') {
            steps {
                // Run the Python script
                sh 'python test.py'
            }
        }
    }
}
