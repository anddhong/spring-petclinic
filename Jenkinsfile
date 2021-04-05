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
        sh '''java -Dserver.port=8888 -jar target/spring-petclinic-2.4.2.jar
'''
      }
    }

  }
}