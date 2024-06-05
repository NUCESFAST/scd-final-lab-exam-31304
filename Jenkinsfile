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
                bat 'docker-compose -f C:\\Users\\samii\\Downloads\\scd-final-lab-exam-31304-master\\scd-final-lab-exam-31304-master\\DockerCompose.yml up --build -d '
            }
        }
        stage('21i-1103 Push') {
            steps {
                //add docker file on docker registery
                bat 'docker push samiirshad1103343/final_lab_exam:latest'
            }
        }
    }
}
