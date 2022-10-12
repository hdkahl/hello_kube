pipeline {
  agent {
    kubernetes {
      inheritFrom 'gcc'
    }
  }
  stages {
    stage('Build') {
      steps {
        container('gcc') {
          sh 'make hello'
        }
      }
    }
    stage('Test') {
      steps {
        container('gcc') {
          sh 'make hello'
          sh 'make test'
        }
      }
    }
  }
}
