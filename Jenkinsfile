pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        sh '''
git pull origin'''
        withGradle() {
          sh 'gradle --version'
        }

      }
    }

  }
}