pipeline {
  agent any
  stages {
    stage('Inittialization') {
      steps {
        sh '''echo PATH = ${PATH}
echo M3_HOME = ${M3}
mvn clean'''
      }
    }
    stage('Build') {
      steps {
        sh '''echo Starting build steps \\n
mvn -Dmaven.test.failure.ignore=true install'''
      }
    }
  }
}