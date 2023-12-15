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
                    sh 'python3 -m venv env'
                    sh 'source env/bin/activate && pip install flask'
                }
            }
        }
        stage('test') {
            steps {
                script {
                    sh 'source env/bin/activate && python test.py'
                }
            }
        }
    }
}
