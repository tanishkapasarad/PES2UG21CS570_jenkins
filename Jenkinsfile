pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                build 'PES2UG21CS570-1'
                sh 'g++ hello.cpp -o output'
            }
        }

        stage('Test') {
            steps {
                sh './test'
            }
        }

        stage('Deploy') {
            steps {
                echo 'deploy'
            }
        }
    }

    post {
        failure {
            echo 'Pipeline failed'
        }
    }
}
