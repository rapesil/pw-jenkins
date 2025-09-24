pipeline {
    agent any
    tools {
        nodejs
    }

    stages {
        stage('Instalando dependências') {
            steps {
                sh 'npm install'
            }
        }
        stage('Test') {
            steps {
                echo 'Testing...'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying...'
            }
        }
    }
}