pipeline {
    agent any

    tools{
        nodejs 'NodeJS'
    }

    stages {
        stage('Instalacao das dependencias') {
            steps {
                echo 'Instalando os pacotes node'
                bat 'npm install'
                bat 'npx cypress install'
            }
        }
    
        stage('Execucao dos testes') {
            steps {
                echo 'Executando os testes'
                bat 'npm test'
            }
        }
    }

    post {
        success {
            echo 'Build e testes executados com sucesso'
        }

        feilure {
            echo 'Falha na execucao do pipeline'
        }
    }
}




