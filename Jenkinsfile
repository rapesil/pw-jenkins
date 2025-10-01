pipeline {
    // agent {
    //     label 'nodejs'  // nome do node configurado no Jenkins
    // }
    agent {
        docker {
            image 'node:20-bookworm'   // ou node:18, conforme seu projeto
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
                sh 'npx -y playwright@1.55.0 install --with-deps'
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