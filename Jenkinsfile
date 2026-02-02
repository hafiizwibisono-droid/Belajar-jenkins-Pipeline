pipeline {
    agent any 

    stages {
        stage("Build") {
            steps {
                echo "Start Build"
                sh "java -version" 
                sh "./mvnw clean compile test-compile"
                echo "Finish Build"
            }
        }

        stage("Build 2") {
            steps {
                echo "Start Test"
                sh "./mvnw test"
                echo "Finish Test"
            }
        }

        stage("Deploy") {
            steps {
                echo "Hello Deploy 1"
                echo "Hello Deploy 2"
            }
        }
    }

    post {
        always {
            echo "I will always say Hello again!"
        }
        success {
            echo "Yay, success"
        }
        failure {
            echo "Oh no, failure"
        }
        cleanup {
            echo "Don't care success or error"
        }
    }
}
