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
   stage ('Publish html') { 
      steps {
        // publish html
        publishHTML target: [
            allowMissing: false,
            alwaysLinkToLastBuild: false,
            keepAll: true,
            reportDir: 'surefire-reports',
            reportFiles: 'client.client.html',
            reportName: 'Mock test report'
          ]
      }
  }
}
