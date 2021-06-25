pipeline {
  agent none
  stages {
    stage('Build') {
      agent {
        docker {
          args '-v /root/.m2:/root/.m2'
          image 'maven:3-alpine'
        }

      }
      steps {
        echo 'build stage'
      }
    }

    stage('test') {
      agent {
        node {
          label 'test'
        }

      }
      steps {
        bat(script: 'E:\\workspace\\eclipse-workspace\\AutomationTest\\run.bat', returnStatus: true, returnStdout: true)
      }
    }

  }
}