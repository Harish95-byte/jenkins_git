pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                bat 'python --version'
            }
        }

        stage('Test') {
            steps {
                bat 'python app.py'
            }
        }
    }

    post {
        success {
            echo "✅ BUILD SUCCESS: Pipeline completed successfully!"
        }
        failure {
            echo "❌ BUILD FAILED: Something went wrong!"
        }
    }
}
