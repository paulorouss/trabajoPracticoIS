pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        sh '''
git pull origin'''
        sh './gradlew bootRun'
      }
    }

    stage('Test') {
      environment {
        CI = 'true'
      }
      steps {
        sh ' ./jenkins/scripts/test.sh'
      }
    }

  }
}