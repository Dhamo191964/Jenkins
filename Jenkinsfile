pipeline {
    agent any

    tools {
        maven 'Maven'   // Jenkins la already configure pannirukanum
    }

    stages {

        stage('Checkout') {
            steps {
                git 'https://github.com/your-username/my-app.git'
            }
        }

        stage('Build') {
            steps {
                bat 'mvn clean compile'
            }
        }

        stage('Test') {
            steps {
                bat 'mvn test'
            }
        }

        stage('Package') {
            steps {
                bat 'mvn package'
            }
        }

        stage('Deploy') {
            steps {
                echo "Deploying application..."

                // Example: run jar locally
                bat 'java -jar target/my-app-1.0.jar'
            }
        }
    }
}
