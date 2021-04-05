pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        echo 'Starting Build'
        sh 'java -jar target/spring-petclinic-2.4.2.jar'
        sh 'mvn clean install -Dlicense.skip=true'
        echo 'build finished'
      }
    }

  }
}