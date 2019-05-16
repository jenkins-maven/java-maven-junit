pipeline {
  agent any
  stages {
    stage('Initialize') {
      steps {
        echo 'Testing the message'
        sh '''echo PATH = ${PATH}
echo M3_HOME = ${M3}
mvn clean'''
      }
    }
    stage('Build') {
      steps {
        sh 'mvn -Dmaven.test.failure.ignore=true install'
      }
    }
  }
}