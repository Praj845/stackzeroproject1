pipeline {
    agent any

    environment {
        DOCKER_HUB_USERNAME = credentials('docker-hub-username')
        DOCKER_HUB_PASSWORD = credentials('docker-hub-password')
    }

    stages {
        // ... (other stages)

        stage('Push to Docker Repository') {
            steps {
                script {
                    docker.withRegistry('https://registry.hub.docker.com', 'docker-hub-credentials-id') {
                        // Use DOCKER_HUB_USERNAME and DOCKER_HUB_PASSWORD as needed
                        dockerImage.push()
                    }
                }
            }
        }

        // ... (other stages)
    }
}

