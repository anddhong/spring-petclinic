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
        sh '''cd /path/to/code/
sonar.projectKey=App Name- Any Identifier
sonar.projectName=Project1
sonar.projectVersion=1.0.0
sonar.projectDescription=Static analysis for the AppName
sonar.sources=path/to/code/src, path/to/code/grails-app
sonar.groovy.cobertura.reportPath=path/to/code/target/test-reports/cobertura/coverage.xml
sonar.language=grvy
sonar.sourceEncoding=UTF-8'''
        echo 'test complete'
      }
    }

  }
}