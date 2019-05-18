pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        sh '''echo mavenHome = \'${M3}\'
mvn package -Dmaven.test.skip=true'''
      }
    }
    stage('deploy') {
      steps {
        sh 'echo JOb_name= \'${env.JOB_NAME}\''
      }
    }
  }
}