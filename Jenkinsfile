pipeline {
    agent { docker { image 'mcr.microsoft.com/playwright:focal' } }
    stages {
        stage ('Test') {
            steps {
                sh 'npm ci'
                sh 'npm test'
            }
        }
    }
}
