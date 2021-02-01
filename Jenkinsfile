pipeline {
    agent any
    tools {
        node 'node-14.15.4'
    }
    stages {
        stage('Test') {
            steps {
                git branch: 'master', url: 'http://10.250.14.1:8929/root/hello-nodejs-testing'
                sh 'yarn'
                sh 'yarn test'
            }
        }
    }
}
