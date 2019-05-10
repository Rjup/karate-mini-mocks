pipeline {
  agent any
  stages {
    stage('Test') {
      steps {
        sh 'mvn clean test'
      }
    }
    stage('Report') {
      steps {
        sh '''tree /var/lib/jenkins/workspace/minmock-cucumber-report_master/target/surefire-reports/ 
'''
      }
    }
  }
}