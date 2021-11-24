pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        sh '''
git pull origin'''
        withGradle() {
          sh 'gradle init'
        }

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