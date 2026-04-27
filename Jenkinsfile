pipeline {
    agent any

    tools {
        maven 'Maven'   // configure in Jenkins tools
    }

    stages {

        stage('Clone Code') {
            steps {
                git 'https://github.com/Dhamu191964/Jenkins.git'
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
    }
}
