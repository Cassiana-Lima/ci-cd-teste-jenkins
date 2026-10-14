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
                stage('Testes da suite 1') {
                    steps {
                        bat 'npm run test-suite-1' 
                    }
                }
                stage('Teste da suite 2') {
                    steps {
                        bat 'npm run test-suite-2' 
                    }
                }

                stage('Teste da suite 2') {
                    steps {
                        bat 'npm run test-suite-' 
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




