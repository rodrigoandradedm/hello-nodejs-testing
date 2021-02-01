pipeline {
    agent any
    tools {
        node 'node:15.7.0-buster'
    }
    stages {
        stage('Test') {
            steps {
                stage{
                    git branch: 'master', url: 'http://10.250.14.1:8929/root/hello-nodejs-testing'
                    sh 'yarn'
                    sh 'yarn test'
                }
            }
        }
    }
}
