pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        sh '''./gradlew build
'''
      }
    }

    stage('') {
      steps {
        sh './gradlew check'
      }
    }

  }
}