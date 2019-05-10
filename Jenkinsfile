pipeline {
  agent any
  stages {
    stage('Test') {
      steps {
        sh 'mvn -X test'
      }
    }
    stage('Report') {
      steps {
        sh '''cp /var/lib/jenkins/workspace/minmock-cucumber-report_master/target/surefire-reports/ /home/centos/mimockReport
'''
      }
    }
  }
}