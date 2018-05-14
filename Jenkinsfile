pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        sh 'npm install'
      }
    }
    stage('Tests') {
      parallel {
        stage('Tests') {
          steps {
            echo 'Performing Chrome Tests'
          }
        }
        stage('Components') {
          steps {
            echo 'Performing Components Tests'
          }
        }
        stage('Integrations') {
          steps {
            echo 'Performing Integrations Tests'
          }
        }
      }
    }
    stage('Browser Tests') {
      parallel {
        stage('Chrome') {
          steps {
            echo 'Performing Chrome Tests'
          }
        }
        stage('Firefox') {
          steps {
            echo 'Performing Firefox Tests'
          }
        }
        stage('Internet Explorer') {
          steps {
            echo 'Performing Internet Explorer Tests'
          }
        }
        stage('Safari') {
          steps {
            echo 'Performing Safari Tests'
          }
        }
      }
    }
    stage('Security Tests') {
      parallel {
        stage('SQL Injections') {
          steps {
            echo 'Performing ZAP Tests'
          }
        }
        stage('Zed Attack Proxy') {
          steps {
            echo 'Performing Zed Attack Proxy Tests'
          }
        }
      }
    }
    stage('Auth Deployment?') {
      steps {
        input 'Deploy this build to Development?'
      }
    }
    stage('Deploy to DEV') {
      steps {
        echo 'Deploying this build to Development...'
      }
    }
  }
}