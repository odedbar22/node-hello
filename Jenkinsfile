pipeline {
  agent {
    node {
      label 'jenkins-docker-slave'
    }

  }
  stages {
    stage('checkout-code') {
      steps {
        git(url: 'https://github.com/odedbar22/node-hello.git', branch: 'master', changelog: true, poll: true)
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