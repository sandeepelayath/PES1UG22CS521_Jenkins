pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                sh 'g++ main/hello.cpp -o main/hello'
            }
        }
        stage('Test') {
            steps {
                sh './main/hello'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying application...'
            }
        }
    }

    post {
        failure {
            echo 'Pipeline failed'
        }
    }
}
