pipeline {
    agent any

    environment {
        PATH = "/opt/sonar-scanner/bin:$PATH"
    }

    stages {
        stage('SonarQube Analysis') {
            steps {
                withSonarQubeEnv('MySonarServer') {
                    sh 'sonar-scanner'
                }
            }
        }

        stage("Quality Gate") {
            steps {
                timeout(time: 2, unit: 'MINUTES') {
                    waitForQualityGate abortPipeline: true
                }
            }
        }
    }
}
