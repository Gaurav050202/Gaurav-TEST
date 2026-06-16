pipeline {
  agent any
  stages {
    stage('Checkout') {
      steps {
        git url: 'https://github.com/Gaurav050202/Gaurav-TEST.git'
      }
    }
    stage('Build') {
      steps {
        sh 'echo Building...'
      }
    }
  }
}
