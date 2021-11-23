pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        sh '''
git pull origin'''
        sh '''stage(\'Gradle Build\') {
    if (isUnix()) {
        sh \'./gradlew clean build\'
    } else {
        bat \'gradlew.bat clean build\'
    }
}'''
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