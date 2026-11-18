pipeline {
    agent {
        docker {
            image 'maven:3.9.6-eclipse-temurin-17'
        }
    }
    stages {
        stage('Checkout') {
            steps {
                checkout scm
            }
        }
        stage('Build Fat JAR') {
            steps {
                sh 'mvn clean package'
            }
        }
    }
    post {
        success {
            echo 'Pipeline completed successfully and fat JAR was built!'
        }
    }
}
