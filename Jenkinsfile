pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                sh 'echo this is a build'
            }
        }
        stage('Test') {
            steps {
                sh 'echo this is a test'
            }
        }
        stage('Deploy') {
            steps {
                echo 'this is a deploy'
            }
        }
    }
}