pipeline {
    agent {
        label 'AGENT-1' 
    }
    options {
                // timeout counter starts BEFORE agent is allocated
            timeout(time: 30, unit: 'MINUTES')
            disableConcurrentBuilds()
    }
    parameters {
        string(name: 'PERSON', defaultValue: 'Mr Jenkins', description: 'Who should I say hello to?')

        text(name: 'BIOGRAPHY', defaultValue: '', description: 'Enter some information about the person')

        booleanParam(name: 'TOGGLE', defaultValue: true, description: 'Toggle this value')

        choice(name: 'CHOICE', choices: ['One', 'Two', 'Three'], description: 'Pick something')

        password(name: 'PASSWORD', defaultValue: 'SECRET', description: 'Enter a password')
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