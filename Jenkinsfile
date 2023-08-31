pipeline {
    agent any
    
    tools {nodejs "mynode"}
    
    stages {
        stage('Build') {
            steps {
                sh 'npm install'
            }
        }
        stage('Test') {
            steps {
              sh 'npm install'
              }
            }
        }
        stage('Deploy') {
            steps {
                echo "Deployed to AWS"
            }
        }
    }