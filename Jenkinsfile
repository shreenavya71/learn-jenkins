pipeline {
    agent {
        label 'AGENT-1' 
    }
    options {
                // timeout counter starts BEFORE agent is allocated
            timeout(time: 30, unit: 'MINUTES')
    }

    stages {
        stage('Build') {
            steps {
                sh 'echo this is a build'
            }
        }
        stage('Test') {
            steps {
                sh 'echo this is a test'
                sh 'sleep 10'
            }
        }
        stage('Deploy') {
            steps {
                echo 'this is a deploy'
            }
        }
    }
}