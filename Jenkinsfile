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
    stage('Get Azure Scripts') {
      steps {
        git(url: 'https://AbdellGautier:Winter0101%21@github.lennar.com/AbdellGautier/azlendeploy-app-angular6.git', branch: 'master')
      }
    }
    stage('Verify Deployment') {
      steps {
        fileExists 'deploy.ps1'
      }
    }
  }
}