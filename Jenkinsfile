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

  }
}