pipeline {
  agent {
    node {
      label 'jenkins-docker-slave'
    }

  }
  stages {
    stage('checkout-code') {
      steps {
        sh 'echo "hello world1"'
      }
    }

    stage('done') {
      steps {
        sh 'echo "done"'
      }
    }

  }
}