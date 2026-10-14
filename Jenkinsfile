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
            parallel {
                stage('Teste no Chrome') {
                    steps {
                        bat 'npm run test-chrome' 
                    }
                }
                stage('Teste no Electron') {
                    steps {
                        bat 'npx cypress run --browser electron' 
                    }
                }
            }
        }
    }

    post {
        success {
            echo 'Build e testes executados com sucesso'
        }

        failure {
            echo 'Falha na execucao do pipeline'
        }
    }
}




