pipeline {

    agent any

    stages {

        stage('Build Docker Image') {
            steps {
                bat 'docker build -t hospital-app .'
            }
        }

        stage('Run Docker Container') {
            steps {
                bat 'docker run -d -p 8082:80 hospital-app'
            }
        }

    }
}