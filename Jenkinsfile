pipeline {
  agent any
  stages {
    stage('sonar') {
      steps {
        withSonarQubeEnv('sonar_scanner') {
          waitForQualityGate true
        }

      }
    }
  }
}