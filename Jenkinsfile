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
        fileExists '/var/lib/jenkins/workspace/karate-mini-mocks_master/target/surefire-reports/client.client.html'
      }
    }
  }
}