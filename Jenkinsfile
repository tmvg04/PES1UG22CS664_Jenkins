pipeline {
    agent any
    stages {
        stage('Clone repository') {
            steps {
                git branch: 'main', url: ''
            }
        }
        stage('Build application') {
            steps {
                sh 'g++ -o PES1UG22CS664-1 main.cpp'
            }
        }
        stage('Test application') {
            steps {
                sh './PES1UG22CS664-1'
            }
        }
        stage('Deploy application') {
            steps {
                echo 'Deploying application...'
            }
        }
    }
    post {
        failure {
            echo 'Pipeline failed!'
        }
        success {
            echo 'Pipeline executed successfully!'
        }
    }
}
