pipeline {
    agent any
    
    tools {nodejs "mynode"}
    
    stages {
        stage('Build') {
            steps {
                sh '/usr/local/bin/node install'
            }
        }
        stage('Test') {
            steps {
              sh '/usr/local/bin/node install'
              }
            }
        
        stage('Deploy') {
            steps {
                echo "Deployed to AWS"
            }
        }
    }
}