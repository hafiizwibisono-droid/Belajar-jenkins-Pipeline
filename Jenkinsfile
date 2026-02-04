pipeline {
    agent {
        node {
            label "linux"
        }
    }

    stages {
        stage("Build") {
            steps {
                echo "Start Build"
                sleep(5)
                sh "./mvnw clean compile test-compile"
                echo "Finish Build"
            }
        }

        stage("Build 2") {
            steps {
                echo "Start Test Stage"
                sh "./mvnw test"
                echo "Finish Test Stage"
            }
        }

        stage("Deploy") {
            steps {
                echo "Hello Deploy 1"
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
