pipeline {
    agent any

    triggers {
        pollSCM('* * * * *')
    }

    stages {
        stage('Checkout') {
            steps {
                git branch: 'main', url: 'https://github.com/Harish95-byte/jenkins_git.git'
            }
        }

        stage('Compile') {
            steps {
                bat 'javac Hello.java'
            }
        }

        stage('Run') {
            steps {
                bat 'java Hello'
            }
        }

        stage('Archive Artifacts') {
            steps {
                archiveArtifacts artifacts: 'Hello.class', fingerprint: true
            }
        }
    }

    post {
        success {
            echo "✅ CI PIPELINE SUCCESS!"
        }
        failure {
            echo "❌ CI PIPELINE FAILED!"
        }
    }
}
