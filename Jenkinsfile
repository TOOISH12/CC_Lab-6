pipeline {
    agent any

    stages {
        stage('Checkout SCM') {
            steps {
                checkout scm
            }
        }

        stage('Build Backend Image') {
            steps {
                echo "Building backend Docker image"
                sh 'docker build -t backend-app ./backend'
            }
        }

        stage('Deploy Backend Containers') {
            steps {
                echo "Deploying backend container"
                sh 'docker rm -f backend || true'
                sh 'docker run -d --name backend backend-app'
            }
        }

        stage('Post Actions') {
            steps {
                echo "Pipeline executed successfully"
            }
        }
    }
}
