pipeline {
    agent any

    tools{
        nodejs 'NodeJS'
    }

    stages {
        stage('Instalacao das dependencias') {
            steps {
                bat 'npm install'
                bat 'npx cypress verify'
            }
        }
    
        stage('Execucao dos testes') {
            steps {
                bat 'npm test'
            }
        }
    }
}




