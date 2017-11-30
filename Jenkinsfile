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
   stage('deploy') {
        agent none
        steps {
            script {
                def customImage = docker.build("thiebaultnonet/maths:${env.BUILD_NUMBER}")
         }
        }
    }
  }
}