pipeline {
    agent any

    stages {
        stage('Checkout Code') {
            steps {
                git branch: 'main',
                    url: 'https://github.com/Viruthebrave/azure-aks-cicd-project.git'
            }
        }

        stage('Verify Files') {
            steps {
                sh 'ls -l'
            }
        }
    }
}
