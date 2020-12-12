pipeline {
    agent none
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
            agent {
                docker { image 'node:14-alpine' }
            }
            steps {
                sh 'node --version'
            }
        }
        stage('list directory') {            
            steps {
                sh 'ls -lrt'
            }
        }
        stage('python version'){
            agent { docker { image 'python:3' } }
            steps{
                sh 'python3 --version'
            }
        }
    }
}
