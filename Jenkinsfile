pipeline {
   agent any
    stages {
        stage('Build') {
            steps {
                sh './gradlew clean'
                sh './gradlew assemble'
            }
            
        }
        stage('Test') {
            steps {
                sh './gradlew test'
            }
        }
        stage('Integration') {
            agent {
                docker { image 'node:14-alpine' }
            }
            steps {
                sh 'node --version'
            }
        }
        
    }
}
