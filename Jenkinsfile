pipeline {
    agent none
    stages {
        stage('test') {
            agent { docker { image 'python:3.9.0' } }
            steps {
                sh 'python --version'
                sh 'exit 1'
            }
        }
        stage('build') {
            agent { docker { image 'python:3.5.1' } }
            steps {
                sh 'python --version'
            }
        }
    }
}
