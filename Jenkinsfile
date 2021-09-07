pipeline {
    agent any
    tools { 
        nodejs 'node14'
    }
    environment {
        NODE_ENV = 'dev'
    }
    stages {
        stage ('Test') {
            steps {
                sh 'npm ci'
                sh 'npm test'
            }
        }
    }
}
