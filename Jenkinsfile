pipeline {
    agent { docker { image 'mcr.microsoft.com/playwright:focal' } }
    stages {
        stage ('Test') {
            steps {
                sh 'export npm_config_cache=$(mktemp -d) && npm ci'
                sh 'npm run test:success'
                sh 'npm run test:failure'
                sh 'rm -rf $npm_config_cache'
            }
        }
    }
}
