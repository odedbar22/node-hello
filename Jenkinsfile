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
        sh '''curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.40.0/install.sh | bash
nvm install 10
node -v 
npm -v'''
      }
    }

    stage('build node pack') {
      steps {
        sh 'npm install'
      }
    }

  }
}