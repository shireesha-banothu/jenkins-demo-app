pipeline {
  agent any

  stages {
    stage('Build Docker Image') {
      steps {
        script {
          docker.build('jenkins-demo-app')
        }
      }
    }

    stage('Run App') {
      steps {
        script {
          docker.image('jenkins-demo-app').run('-p 3000:3000')
        }
      }
    }
  }
}

