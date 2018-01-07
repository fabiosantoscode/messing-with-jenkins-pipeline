pipeline {
    agent any;

    stages {
        stage('Build') {
            steps {
                sh 'echo hello world'
            }
        }

        stage('Build 2') {
            steps {
                sh 'echo hi again, gonna fail'
                sh 'false'
            }
        }

        stage('Produce some artifacts') {
            steps {
                sh 'echo hello world > artifact.txt'
                archive includes: 'artifact.txt'
            }
        }
    }
}
