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
                bat 'docker tag scd-final-lab-exam-31304-master-21i-1103_backend4:latest samiirshad1103343/scd-final-lab-exam-31304-master-21i-1103_backend4:latest'
                bat 'docker push samiirshad1103343/scd-final-lab-exam-31304-master-21i-1103_backend4:latest'
                 bat 'docker tag scd-final-lab-exam-31304-master-21i-1103_backend3:latest samiirshad1103343/scd-final-lab-exam-31304-master-21i-1103_backend3:latest'
                bat 'docker push samiirshad1103343/scd-final-lab-exam-31304-master-21i-1103_backend3:latest'
                
                 bat 'docker tag scd-final-lab-exam-31304-master-21i-1103_backend2:latest samiirshad1103343/scd-final-lab-exam-31304-master-21i-1103_backend2:latest'
                bat 'docker push samiirshad1103343/scd-final-lab-exam-31304-master-21i-1103_backend2:latest'
                
                 bat 'docker tag scd-final-lab-exam-31304-master-21i-1103_backend1:latest samiirshad1103343/scd-final-lab-exam-31304-master-21i-1103_backend1:latest'
                bat 'docker push samiirshad1103343/scd-final-lab-exam-31304-master-21i-1103_backend1:latest'
                
            
            }
        }
    }
}
