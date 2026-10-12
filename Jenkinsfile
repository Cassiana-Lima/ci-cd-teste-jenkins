pipeline {
    agent any

    tools{
        nodejs 'NodeJS'
    }

    environment {
        CYPRESS_CACHE_FOLDER = "${WORKSPACE}\\.cypress-cache"
    }

    stages {
        stage('Instalacao das dependencias') {
            steps {
                bat 'npm install'
                bat 'npx cypress install'
            }
        }
    
        stage('Execucao dos testes') {
            steps {
                bat 'npm test'
            }
        }
    }
}




