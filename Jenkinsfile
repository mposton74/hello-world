pipeline {
    agent {
        docker { image 'node:14-alpine' }
    }
    stages {
        stage('Back-end') {
            steps {
                echo 'hello from back end'
            }
        }
        stage('Front-end') {
            steps {
                echo 'hello from front end'
            }
        }
        stage('Test') {
            steps {
                sh 'node --version'
            }
        }
        stage('list directory') {            
            steps {
                sh 'ls -lrt'
            }
        }
    }
}
