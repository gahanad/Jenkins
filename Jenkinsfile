pipeline {
    agent any

    stages {
        stage('Clone') {
            steps {
                git 'https://github.com/gahanad/Jenkins.git'
            }
        }

        stage('Build Docker Image') {
            steps {
                sh 'docker build -t cc-backend ./backend'
            }
        }

        stage('Run Container') {
            steps {
                sh 'docker run -d --name cc-backend-container cc-backend'
            }
        }
    }
}