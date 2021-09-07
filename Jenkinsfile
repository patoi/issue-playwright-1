pipeline {
    agent { docker { image 'mcr.microsoft.com/playwright:focal' } }
    stages {
        stage ('Test') {
            steps {
                sh 'mkdir .npm && chown -R 501:20 "/.npm"'
                sh 'npm ci'
                sh 'npm test'
            }
        }
    }
}
