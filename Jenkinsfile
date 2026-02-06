pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                echo "Code is already checked out from SCM"
            }
        }

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
}
