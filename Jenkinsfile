pipeline {
    agent any

    stages {
        stage('Pull Code') {
            steps {
                git 'https://github.com/YOUR-USERNAME/jenkins-docker-app.git'
            }
        }

        stage('Build Image') {
            steps {
                sh 'docker build -t my-app .'
            }
        }

        stage('Run Container') {
            steps {
                sh 'docker run -d -p 3000:3000 --name my-app my-app'
            }
        }

        stage('Check') {
            steps {
                sh 'docker ps'
            }
        }
    }
}
