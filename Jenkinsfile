pipeline {
  agent {
    node {
      label 'test'
    }

  }
  stages {
    stage('test') {
      steps {
        bat(script: 'E:\\workspace\\eclipse-workspace\\AutomationTest\\run.bat', returnStatus: true, returnStdout: true)
      }
    }

  }
}