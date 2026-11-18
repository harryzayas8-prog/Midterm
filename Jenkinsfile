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
                sh './mvnw clean package'
            }
        }
    }
    post {
        success {
            echo 'Pipeline completed successfully and fat JAR was built!'
        }
    }
}
EOF
