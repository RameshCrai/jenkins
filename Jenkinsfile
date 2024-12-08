pipeline {
    agent any
    stages {
        stage('Clone Repo') {
            steps {
                sh 'rm -Rf 730am'
                sh 'git clone https://github.com/SUSIGUGH/730am.git'
            }
        }
        stage('Build Docker Image') {
            steps {
                sh '''
                cd 730am/docker
                sudo docker build -t httpdimg .
                '''
            }
        }
    }
}
