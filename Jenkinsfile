pipeline {
    agent any

    environment {
        IMAGE_NAME = "release-demo"
        IMAGE_TAG = "${BUILD_NUMBER}"
    }

    stages {

        stage('Cloning Repository') {
            steps {
                git ''
            }
        }

        stage('Build Docker Image') {
            steps {
                sh 'docker build -t $IMAGE_NAME:$IMAGE_TAG .'
            }
        }

        stage('Verify Image') {
            steps {
                sh 'docker images'
            }
        }

    }

 
}