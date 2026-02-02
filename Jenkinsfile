pipeline {
    agent any

    stages {
        stage("Build") {
            steps {
                echo "Memulai Build..."
                sh "./mvnw clean compile test-compile"
            }
        }
        stage("Test") {
            steps {
                sh "./mvnw test"
            }
        }
        stage("Deploy") {
            steps {
                echo "Deploying..."
            }
        }
    }

    post {
        always {
            echo "Pipeline selesai."
        }
    }
}
