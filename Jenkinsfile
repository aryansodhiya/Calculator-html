pipeline {
    agent any
    stages {
        stage('Checkout Code') {
            steps {
                git credentialsId: 'b4a9b5da-6b96-4a35-9818-48bbbf82ce9b', url: 'https://github.com/aryansodhiya/Calculator-html.git'
            }
        }
        stage('Deploy to Nginx') {
            steps {
                
                //Or use rsync for remote deployments.
                sh 'rsync -avz index.html user@nginx-server:/usr/share/nginx/html/'
            }
        }
    }
}
