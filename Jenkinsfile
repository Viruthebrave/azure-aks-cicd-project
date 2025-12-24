pipeline {
    agent any

    stages {
        stage('Checkout Code') {
            steps {
                git branch: 'main',
                    url: 'https://github.com/Viruthebrave/azure-aks-cicd-project.git'
            }
        }

        stage('Build Docker Image') {
            steps {
                sh '''
                  docker build -t azure-cicd-app:latest .
                '''
            }
        }

        stage('Verify Docker Image') {
            steps {
                sh '''
                  docker images | grep azure-cicd-app
                '''
            }
        }
    }
}
