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
                    sh 'python -m venv venv'
                    sh '. venv\\Scripts\\activate && pip install flask'
                }
            }
        }
        stage('test') {
            steps {
                script {
                    sh 'python -m venv venv'
                    sh '. venv\\Scripts\\activate && python test.py'
                }
            }
        }
    }
}
