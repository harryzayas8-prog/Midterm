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
                dir('complete') {
                    sh 'mvn clean package -DskipTests'
                }
            }
        }
    }
    post {
        success {
            echo 'Pipeline completed successfully and fat JAR was built!'
        }
    }
}
