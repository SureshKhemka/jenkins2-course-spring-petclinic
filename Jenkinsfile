pipeline {
    agent any
    stages {
        stage('Checkout') {
            steps {
                checkout scm
            }
        }
        stage('Build') {
            steps {
                sh './mvnw clean package -DskipTests=true'
            }
        }
        stage('Deploy') {
            steps {
                sh './mvnw deploy'
            }
        }
    }
}
