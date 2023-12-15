pipeline {
    agent {
        docker {
            image 'python:3.7.2'
        }
    }
    stages {
        stage('build') {
            steps {
                script {
                    sh 'virtualenv venv'
                    sh 'source venv/bin/activate && pip install flask'
                }
            }
        }
        stage('test') {
            steps {
                script {
                    sh 'virtualenv venv'
                    sh 'source venv/bin/activate && python test.py'
                }
            }
        }
    }
}
