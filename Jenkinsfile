pipeline {
  agent { docker 'maven:3.5-alpine'}
  stages {
    stage ('Checkout') {
      steps {
        git 'https://github.com/effectivejenkins/spring-petclinic'
      }
    }
    stage('build') {
      steps {
      sh 'mvn clean package'
      junit '**/target/surefire-resports/Test-*.xml'
      }
    }
  }
}
