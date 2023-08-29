pipeline {
    agent any
    
    stages {
        stage('Build and Run Graylog') {
            steps {
                // Clone your repository or pull updates
                checkout scm

                // Build and start Graylog using Docker Compose
                sh 'docker-compose up -d'
            }
        }
    }
    
    // No "post" section here, so the containers will remain running
}
