pipeline {

    agent any

    stages {

        stage('Checkout Code') {

            steps {

                git credentialsId: 'b4a9b5da-6b96-4a35-9818-48bbbf82ce9b', url: 'https://github.com/aryansodhiya/Calculator-html.git'

            }

        }

        stage('Build Docker Image') {

            steps {

                sh 'docker build -t docker-cal-app .'

            }

        }

        stage('Deploy Docker Container') {

            steps {

                sh 'docker stop docker-cal-app || true'

                sh 'docker rm docker-cal-app|| true'

                sh 'docker run -d -p 8080:80 --name  docker-cal-app'

            }

        }

    }

}
