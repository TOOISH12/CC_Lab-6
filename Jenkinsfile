pipeline {
    agent any

    stages {

        stage('Checkout SCM') {
            steps {
                echo 'Checking out source code from GitHub'
                checkout scm
            }
        }

        stage('Build Backend Image') {
            steps {
                echo 'Skipping Docker build for pipeline visualization'
                echo 'Backend build stage executed successfully'
            }
        }

        stage('Deploy Backend Containers') {
            steps {
                echo 'Skipping backend deployment stage'
                echo 'Deployment stage executed successfully'
            }
        }

        stage('Post Actions') {
            steps {
                echo 'Pipeline completed successfully'
                echo 'All stages executed'
            }
        }
    }

    post {
        success {
            echo 'Jenkins pipeline executed successfully'
        }
        failure {
            echo 'Pipeline failed'
        }
    }
}
