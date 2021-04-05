pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        echo 'Starting Build'
        sh '''./mvnw package
'''
        echo 'build finished'
      }
    }

  }
}