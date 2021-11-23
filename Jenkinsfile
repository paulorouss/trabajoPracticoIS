pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        sh '''
git pull origin'''
        sh 'gradle build'
        sh './gradlew bootRun'
      }
    }

  }
}