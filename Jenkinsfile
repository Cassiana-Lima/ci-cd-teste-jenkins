pipeline {
    agent any

    tools{
        nodejs 'NodeJS'
    }

    stages {
        stage('Instalacao das dependencias') {
            steps {
                bat 'npm install'
            }
        }
    
        stage('Execucao dos testes') {
            steps {
                bat 'npm test'
            }
        }
    }
}




