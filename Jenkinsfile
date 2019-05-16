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
      	sh 'Starting build steps'
        sh 'mvn -Dmaven.test.failure.ignore=true install'
      }
    }
  }
}