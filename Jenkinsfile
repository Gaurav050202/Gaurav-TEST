node {
    stage('Checkout') {
        git branch: 'main', url: 'https://github.com/Gaurav050202/Gaurav-TEST.git'
    }

    stage('Unit Tests') {
        try {
            // Run tests (Maven example)
            bat 'mvn test'
        } finally {
            // Publish JUnit results
            junit '**/target/surefire-reports/*.xml'
        }
    }

    stage('Build Docker Image') {
        bat 'docker build -t myproject:latest .'
    }
}
