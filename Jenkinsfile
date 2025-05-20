pipeline {
    agent any
    stages {
        stage('Checkout') {
            steps {
               git branch: 'main', url: 'https://github.com/NambariGayatri/jenkinsCI-CD.git' 
            }
        }
        stage('Build') {
            steps {
              echo 'skipping the build' 
            }
        }
        stage('Test') {
            steps {
              echo 'skipping the test'
            }
        }
        stage('Deploy') {
            steps {
              sh 'sudo apt-get update && sudo apt-get install -y nginx'
              sh 'sudo cp index.html /var/www/html/'
              sh 'sudo systemctl restart nginx'
            }
        }

    }
}