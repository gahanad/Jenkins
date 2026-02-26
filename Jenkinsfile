pipeline {
    agent any

    stages {
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