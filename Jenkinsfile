pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                git 'https://github.com/rayen-haj-hsine/nodejs-getting-started.git'

            }
        }

        stage('Build') {
            steps {
                sh 'npm install'
            }
        }

        stage('Test') {
            steps {
                sh 'npm test'
            }
        }

        stage('Archive') {
            steps {
                archiveArtifacts artifacts: '**/*.zip', allowEmptyArchive: true
            }
        }
    }
}
