pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        mail(subject: 'Job \'${env.JOB_NAME}\' (${env.BUILD_NUMBER}) is waiting for input', body: 'Please go to ${env.BUILD_URL} for more information.', from: 'Jenkins Development', to: 'abdell.gautier@lennar.com')
        sh 'npm install'
      }
    }
    stage('Test') {
      steps {
        sh './jenkins/scripts/test.sh'
      }
    }
  }
}