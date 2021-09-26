pipeline {
  agent {
    docker {
      image 'node:16-buster-slim'
      args '-p 3000:3000'
    }

  }
  environment {
        CI = 'true' 
  }
  stages {
    stage('Build') {
      steps {
        sh 'npm install'
      }
    }

    stage('Test') {
      steps {
        echo 'Test Running'
      }
    }

    stage('Deliver') {
      steps {
        sh 'npm build'
      }
    }

  }
}