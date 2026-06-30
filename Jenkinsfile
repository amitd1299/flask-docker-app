pipeline {
    agent any

    environment {
        IMAGE_NAME = "flask-app"
    }

    stages {

        stage('Checkout Code') {
            steps {
                checkout scm
            }
        }

        stage('Build Docker Image') {
            steps {
                sh 'docker build -t $IMAGE_NAME .'
            }
        }

        stage('Deploy to Dev') {
            steps {
                sh '''
                    docker rm -f flask-dev || true
                    docker run -d --name flask-dev -p 5000:5000 $IMAGE_NAME
                '''
            }
        }

        stage('Approval for Staging') {
            steps {
                input message: 'Deploy to Staging?'
            }
        }

        stage('Deploy to Staging') {
            steps {
                sh '''
                    docker rm -f flask-staging || true
                    docker run -d --name flask-staging -p 5001:5000 $IMAGE_NAME
                '''
            }
        }

        stage('Approval for Production') {
            steps {
                input message: 'Deploy to Production?'
            }
        }

        stage('Deploy to Production') {
            steps {
                sh '''
                    docker rm -f flask-prod || true
                    docker run -d --name flask-prod -p 5002:5000 $IMAGE_NAME
                '''
            }
        }
    }

    post {
        success {
            echo 'Pipeline completed successfully!'
        }
        failure {
            echo 'Pipeline failed.'
        }
    }
}
