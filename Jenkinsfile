pipeline {
  agent { docker 'maven:3.5-alpine'}
  stages {
    stage ('Checkout') {
      steps {
        git 'https://github.com/hooryash/vicks-jks.git'
      }
    }
    stage('build') {
      steps {
      sh 'mvn clean package'
      junit '$WORKSPACE/target/surefire-reports/TEST-*.xml'
      }
    }
  }
}
