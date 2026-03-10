pipeline {
    agent any

    stages {

        stage('Checkout') {
            steps {
                git 'https://github.com/git17615/sample-node-app.git'
            }
        }

        stage('Install Dependencies') {
            steps {
                sh 'npm install'
            }
        }

        stage('Run Tests') {
            steps {
                sh 'npm test'
            }
        }

        stage('Build Docker Image') {
            steps {
                sh 'docker build -t sample-node-app .'
            }
        }

    }
}
