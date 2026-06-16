pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                git branch: 'main', url: 'https://github.com/Gaurav050202/Gaurav-TEST.git'
            }
        }

        stage('Unit Tests') {
            steps {
                // Run tests (Maven example)
                bat 'mvn test'
            }
            post {
                always {
                    // Publish JUnit results
                    junit '**/target/surefire-reports/*.xml'
                }
            }
        }

        stage('Build Docker Image') {
            steps {
                bat 'docker build -t myproject:latest .'
            }
        }
    }
}
