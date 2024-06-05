pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                git 'https://github.com/31304/lab12.git'
            }
        }
        stage('21i-1103 Dependency Installation') {
            steps {
                bat 'npm install'
            }
        }
        stage('21i-1103 Build') {
            steps {
                bat 'docker-compose -f DockerCompose.yml up --build -d'
            }
        }
        stage('21i-1103  Push') {
            steps {
                bat 'docker push frontend'
            }
        }
    }
}
