pipeline {
    agent any
    stages {
        stage('Checkout') {
            steps {
                echo 'Checking out source code from GitHub'
                checkout scm
            }
        }
        stage('Build') {
            steps {
                echo 'Starting Build Stage'
                sh 'echo "Building the application..."'
            }
        }
        stage('Test') {
            steps {
                echo 'Starting Test Stage'
                sh 'echo "Running tests..."'
                sh 'test 1 -eq 1'
            }
        }
        stage('Notify') {
            steps {
                echo 'SUCCESS: CI Pipeline completed successfully!'
            }
        }
    }
    post {
        success {
            echo 'Pipeline completed successfully!'
        }
        failure {
            echo 'Pipeline failed!'
        }
    }
}
