pipeline {
    agent any

    tools{
        nodejs 'NodeJS'
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




