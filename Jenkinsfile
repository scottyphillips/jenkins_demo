pipeline {
    agent none
    stages {
        stage('mil') {
            agent { docker { image 'python:3.9.0' } }
            when {
                branch 'mil'
            }
            steps {
                sh 'python --version'
                sh 'python hello_world.py'
            }
        }
        stage('dcil') {
            agent { docker { image 'python:3.5.1' } }
            when {
                branch 'dcil'
            }
            steps {
                sh 'python --version'
                sh 'python hello_world.py'
            }
        }
        stage('production') {
            agent { docker { image 'python:3.5.1' } }
            when {
                branch 'main'
            }
            steps {
                sh 'python --version'
            }
        }
    }
}
