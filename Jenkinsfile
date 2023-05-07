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
        
    }
    triggers {
        // Poll the Github repository every 5 minutes
        pollSCM '*/5 * * * *'
    }
}
