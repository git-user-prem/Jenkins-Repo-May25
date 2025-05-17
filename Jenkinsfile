pipeline {
    agent any

    environment {
        IMAGE_NAME = "jenkins-demo"
        IMAGE_TAG = "v1"
    }

    stages {
        stage('Clone') {
            steps {
                git url: 'https://github.com/git-user-prem/Jenkins-Repo-May25.git'  // or use local repo path
            }
        }

        stage('Build Docker Image') {
            steps {
                script {
                    sh 'docker build -t $IMAGE_NAME:$IMAGE_TAG .'
                }
            }
        }

         stage('List Docker Images') {
             steps {
                 sh 'docker images'
            }
        }
    }
}

