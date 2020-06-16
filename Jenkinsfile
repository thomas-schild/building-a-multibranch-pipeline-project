// sample NodeJS based project used in https://www.jenkins.io/doc/tutorials/build-a-multibranch-pipeline-project/
pipeline {
    agent {
        docker {
            image: 'node:6-alpine'
            args: '-p 3000:3000 -p 5000:5000'
        }
    }
    stages {
        stage('Prepare') {
            steps {
                sh 'npm install'
            }
        }
        stage('Build') {
            steps {
                sh 'echo "building..."'
            }
        }
        stage('Test') {
            steps {
                sh './jenkins/scripts/test.sh'
            }
        }
    }
}
