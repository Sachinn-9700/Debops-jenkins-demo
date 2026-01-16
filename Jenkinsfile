// Reusable Jenkins Pipeline
// Only change environment values when reusing this pipeline

pipeline {
    agent any

    // Environment variables
    environment {
        PATH = "$PATH:/usr/local/bin/"

        // Credentials from Jenkins global credentials
        DOCKER_HUB_TOKEN = credentials("docker_hub_token")

        // Git repository URL
        GIT_REPO_URL = "https://github.com/Sachinn-9700/Debops-jenkins-demo/"

        // Docker image name 
        
        DOCKER_IMAGE_NAME = 'sachinn9700/myapp:v4'
    }

    stages {

        stage('Build Docker Image') {
            steps {
                echo 'Building Docker image'
                sh "docker build -t ${DOCKER_IMAGE_NAME} ."
            }
        }

        stage('Docker Hub Login') {
            steps {
                echo 'Logging in to Docker Hub'
                 sh 'echo "$DOCKER_HUB_TOKEN" | docker login -u sachinn9700 --password-stdin'
            }
        }

        stage('Push Image to Docker Hub') {
            steps {
                echo 'Pushing Docker image to Docker Hub'
                sh "docker push ${DOCKER_IMAGE_NAME}"
            }
        }

        stage('updating deployment') {
            steps {
                echo 'deploying website throught k8'
                sh "kubeclt apply -f deployment.yaml"
            }
        }
    }
}
