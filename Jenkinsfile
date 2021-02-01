pipeline {
    agent any
    tools {
        nodejs 'node-14.15.4'
    }
    stages {
        stage('Test') {
            steps {
                git branch: 'master', url: 'http://10.250.14.1:8929/root/hello-nodejs-testing'
                sh 'npm i -D tap-junit'
                sh 'yarn'
                sh 'yarn run test | ./node_modules/tap-junit/bin/tap-junit --output output/test'
            }
        }
    }
}
