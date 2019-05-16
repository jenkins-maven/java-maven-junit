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
        sh '''
mvn -Dmaven.test.failure.ignore=true install'''
        mail(subject: 'Build Success', from: 'zakram@microfocus.com', charset: 'UTF-8', mimeType: 'Text/HTML', to: 'konda@microfocus.com', body: 'Build Success Thanks & Regards')
      }
    }
  }
}