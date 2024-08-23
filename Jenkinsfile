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
    environment {
        DEPLOY_TO = 'production'
        GREETINGS = 'Good morning' 
    }

    stages {
        stage('Build') {
            steps {
                sh 'echo this is a build'
                sh 'env'
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
        stage('print params') {
            steps {
                echo "Hello ${params.PERSON}"
                echo "Biography: ${params.BIOGRAPHY}"
                echo "Toggle: ${params.TOGGLE}"
                echo "Choice: ${params.CHOICE}"
                echo "Password: ${params.PASSWORD}"
                echo "triggered test"
            }
        }
    }
}