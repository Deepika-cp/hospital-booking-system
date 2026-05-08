pipeline {

    agent any

    stages {

        stage('Build Docker Image') {
            steps {
                bat 'docker build -t hospital-app .'
            }
        }

        stage('Stop Old Container') {
            steps {
                bat 'docker stop hospital-container || exit 0'
                bat 'docker rm hospital-container || exit 0'
            }
        }

        stage('Run Docker Container') {
            steps {
                bat 'docker run -d --name hospital-container -p 8082:80 hospital-app'
            }
        }

    }
}