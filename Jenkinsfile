pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                sh 'sudo docker build -t app:test .'
            }
        }
        stage('Test') {
            steps {
                echo 'TEST'
            }
        }
        stage('Deploy') {
            steps {
                echo 'DEPLOY'
            }
        }
    }
}
