pipeline {
  agent any
  stages {
    stage('error') {
      steps {
        withSonarQubeEnv('sonar_scanner') {
          waitForQualityGate true
        }

      }
    }
  }
}