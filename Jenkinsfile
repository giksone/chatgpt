pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                echo 'Récupération du code depuis GitHub...'
                checkout scm
            }
        }
        stage('Install') {
            steps {
                echo 'Installation des dépendances...'
                sh 'npm install'
            }
        }
        stage('Test') {
            steps {
                echo 'Exécution des tests...'
                sh 'npm test'
            }
        }
    }
}
