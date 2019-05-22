pipeline {
  agent any
  stages {
    stage('mock test') {
      steps {
        sh 'mvn -X test '
      }
    }
    stage('Report') {
      steps {
        sh '''cd /var/lib/jenkins/workspace/karate-mini-mocks_master/
tree'''
      }
    }
    stage('Publish html') {
      steps {
        publishHTML([            allowMissing: false,            alwaysLinkToLastBuild: false,            keepAll: true,            reportDir: '/var/lib/jenkins/workspace/karate-mini-mocks_master/target/surefire-reports',            reportFiles: 'client.client.html',            reportName: 'Mock test report'          ])
      }
    }
  }
}