pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        sh '''echo mavenHome = \'${M3}\'
mvn package -Dmaven.test.skip=true'''
      }
    }
  }
}