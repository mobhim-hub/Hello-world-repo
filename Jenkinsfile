pipeline {
    agent any

    stages {
        stage('First Hello') {
            steps {
                echo 'Hello, World'
            }
        }

        stage('Wait') {
            steps {
                echo 'Waiting for 20 seconds...'
                sleep time: 20, unit: 'SECONDS'
            }
        }

        stage('Second Hello') {
            steps {
                echo 'Hello, World'
            }
        }
    }
}
