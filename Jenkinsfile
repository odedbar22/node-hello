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

    stage('install node.js') {
      steps {
        sh '''wget https://nodejs.org/dist/v10.24.1/node-v10.24.1-linux-x64.tar.xz
tar -xzvf node-v10.24.1-linux-x64.tar.xz node/
ls node/
  '''
      }
    }

    stage('build node pack') {
      steps {
        sh './node/bin/npm install'
      }
    }

  }
}