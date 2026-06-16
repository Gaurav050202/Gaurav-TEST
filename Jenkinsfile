node {
  stage('Checkout') {
    git branch: 'main', url: 'https://github.com/Gaurav050202/Gaurav-TEST.git'
  }

  stage('Build') {
    bat 'echo Building...'   // use bat on Windows, sh is for Linux
  }
}
