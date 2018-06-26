pipeline {
  agent any
  stages {
    stage('Build') {
      parallel {
        stage('Build') {
          steps {
            sh 'npm install'
          }
        }
        stage('error') {
          steps {
            echo 'Running the Jenkins Build with Willy!'
          }
        }
      }
    }
  }
}