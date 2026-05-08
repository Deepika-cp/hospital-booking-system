pipeline {

    agent any

    stages {

        stage('Clone Repository') {
            steps {
                git 'https://github.com/Deepika-cp/hospital-booking-system.git'
            }
        }

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