pipeline {
    agent any

    stages {
        stage('Build Docker Image') {
            steps {
                script {
                    sh 'docker build -t siri1419/jenkins-demo-app .'
                }
            }
        }

        stage('Run App') {
            steps {
                script {
                    sh 'docker run -d -p 3000:3000 siri1419/jenkins-demo-app'
                }
            }
        }
    }
}
