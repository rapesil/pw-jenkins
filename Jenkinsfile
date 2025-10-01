pipeline {
    // agent {
    //     label 'nodejs'  // nome do node configurado no Jenkins
    // }
    agent {
        docker {
            image 'node:20-alpine'   // ou node:18, conforme seu projeto
            args '-u root:root'      // opcional p/ permissões em cache
        }
    }

    stages {
        stage('Instalando dependências') {
            steps {
                sh 'npm install'
            }
        }
        stage('Test') {
            steps {
                sh 'npx playwright test'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying...'
            }
        }
    }
}