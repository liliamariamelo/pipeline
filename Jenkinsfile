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
                    sh 'python -m venv env'
                    sh '. env/bin/activate && pip install flask'
                }
            }
        }
        stage('test') {
            steps {
                script {
                    sh '. env/bin/activate && python test.py'
                }
            }
        }
    }
}
