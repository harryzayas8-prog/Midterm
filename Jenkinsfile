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
                // This will use the system Maven or wrapper depending on what's installed
                sh 'mvn clean package -DskipTests'
            }
        }
    }
    post {
        success {
            echo 'Pipeline completed successfully and fat JAR was built!'
        }
    }
}
