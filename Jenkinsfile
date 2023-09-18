pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                // Checkout the Git repository
                checkout scm
            }
        }

        stage('Build and Run Python Script') {
            steps {
                script {
                    // Set up a virtual environment (optional but recommended)
                    sh 'python -m venv venv'
                    sh 'source venv/bin/activate'
                    
                    // Install any required dependencies (if needed)
                    // sh 'pip install -r requirements.txt'

                    // Run the Python script
                    sh 'python test.py'
                }
            }
        }
    }

    post {
        always {
            // Clean up (deactivate the virtual environment if used)
            sh 'deactivate'
        }
    }
}
