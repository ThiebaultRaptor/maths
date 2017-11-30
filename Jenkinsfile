pipeline {
  agent any
  stages {
    stage('Testing') {
      agent {
        docker {
            image 'golang'
        }
      }
      steps {
        sh 'go test'
      }
    }
  }
}