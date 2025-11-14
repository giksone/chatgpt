pipeline {
    agent any

    tools {
        nodejs 'NodeJS' // Nom configuré dans Jenkins
    }

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
                // Installe uniquement si package.json existe
                sh 'if [ -f package.json ]; then npm install; fi'
            }
        }

        stage('Run index.js') {
            steps {
                echo 'Exécution de index.js...'
                sh 'node index.js'
            }
        }
    }
}

