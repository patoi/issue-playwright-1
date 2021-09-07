pipeline {
    agent { docker { image 'mcr.microsoft.com/playwright:focal' } }
    stages {
        stage ('Test') {
            steps {
                sh 'export npm_config_cache=$(mktemp -d)'
                sh 'npm ci'
                sh 'npm test'
                sh 'rm -rf $npm_config_cache'
            }
        }
    }
}
