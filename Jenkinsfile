pipeline {
    agent any
    tools {
        node 'node:latest'
    }
    stages {
        stage('Test') {
            steps {
                git branch: 'master', url: 'http://10.250.14.1:8929/root/hello-nodejs-testing'
                sh 'npm add yarn'
                sh 'yarn'
                sh 'yarn test'
            }
        }
    }
}
