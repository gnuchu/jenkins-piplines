#!groovy

node {
  stage('Unit Test') {
    checkout scm
    sh 'node test-server.js &'
    PAGE_OUTPUT = sh (
      script: 'curl localhost:8888',
      returnStdout: true
    ).trim()

    echo "${PAGE_OUTPUT}"
  }
}