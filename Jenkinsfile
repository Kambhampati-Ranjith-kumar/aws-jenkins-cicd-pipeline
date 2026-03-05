pipeline {

    agent any

    stages {

        stage('Clone Repository') {
            steps {
                git 'https://github.com/Kambhampati-Ranjith-kumar/aws-jenkins-cicd-pipeline.git'
            }
        }

        stage('Build Docker Image') {
            steps {
                sh 'docker build -t cicd-node-app .'
            }
        }

        stage('Stop Existing Container') {
            steps {
                sh 'docker stop cicd-node-app || true'
                sh 'docker rm cicd-node-app || true'
            }
        }

        stage('Run Docker Container') {
            steps {
                sh 'docker run -d -p 80:3000 --name cicd-node-app cicd-node-app'
            }
        }

    }
}
