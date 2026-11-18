pipeline {
    agent any
    stages {
        stage('Checkout') {
            steps {
                checkout scm
            }
        }
        stage('Build Fat JAR') {
            steps {
                // Use system maven instead of maven wrapper
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
