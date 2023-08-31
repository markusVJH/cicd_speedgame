pipeline {
    agent any

    tools {nodejs "node"}
    
    stages {
        stage('Checkout') {
            steps {
                // Checkout the source code from the Git repository
                // You might need to configure credentials if the repository is private
                script {
                    checkout scm
                }
            }
        }
         stages {
        stage('Build') {
            steps {
                // Install project dependencies and build the React app
                sh 'npm install'
                sh 'npm run build'
            }
        }
        
        stage('Test') {
            steps {
                // Run tests for your React app
                sh 'npm test'
            }
        }
        
        stage('Deploy') {
            steps {
                // Example deployment step
                // This could be deploying to a server, a hosting platform, etc.
                // Adjust the deployment process based on your setup
                sh 'npm run deploy'
            }
        }
    }
    
    post {
        always {
            // Archive build artifacts, clean up, or perform other cleanup actions
            archiveArtifacts artifacts: 'build/**', allowEmptyArchive: true
        }
        
        success {
            // This block runs when the pipeline is successful
            echo 'Pipeline succeeded!'
        }
        
        failure {
            // This block runs when the pipeline fails
            echo 'Pipeline failed!'
        }
    }
}
}