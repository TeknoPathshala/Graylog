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
    
    post {
        always {
            // Clean up resources, stop containers, etc.
            sh 'docker-compose down'
        }
    }
}
