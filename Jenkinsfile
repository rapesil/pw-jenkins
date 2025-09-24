pipeline {
    agent any
    tools {
        nodejs 'node20'
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