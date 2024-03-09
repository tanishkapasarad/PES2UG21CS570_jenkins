pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                sh 'g++ hello.cpp -o output'
                echo'build successful!'
            }
        }
        stage('Test') {
            steps {
                sh './test'
                echo'test successful!'
            }
        }

        stage('Deploy') {
            steps {
                echo 'deployed!'
            }
        }
    }

    post {
        failure {
            echo 'Pipeline failed'
        }
    }
}
