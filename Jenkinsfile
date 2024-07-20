pipeline {
    agent any

    stages {
        stage('Hello') {
            steps {
                echo 'Hello World'
            }
        }
        stage('Python version') {
            steps {
                echo 'Python version: '
                sh 'python3 --version'
            }
        }
        stage('Pip version') {
            steps {
                echo 'pip version'
                sh 'pip --version'
            }
        }
        stage('create python virtual env'){
            steps {
            sh 'python3 -m venv tutorial-env'
            }
        }
        stage('activate python virtual env'){
            steps {
            sh 'source tutorial-env/bin/activate'
            sh 'python3 -m pip list'
            sh 'python3 -m pip install -r requirements.txt'
            sh 'python3 -m pip list'
            }
        }
/*         stage('list pip packages'){
            sh 'python3 -m pip list'
        }
        stage('install packages for pip'){
            sh 'python3 -m pip install -r requirements.txt'
        }
        stage('list pip packages'){
            sh 'python3 -m pip list'
        } */
    }
}
