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

    stage('Testing') {
      steps {
        echo 'beginning testing'
        sh '''mvn sonar:sonar -Dsonar.host.url=http://192.168.33.10:8081 -Dlicense.skip=true
'''
        echo 'test complete'
      }
    }

  }
}