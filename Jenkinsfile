pipeline {
  agent {
    docker {
      args '-v /opt/cloudhost/apps/mavenRepo:/root/.m2'
      image 'maven:3.3.9-jdk-8'
    }

  }
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