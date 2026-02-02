
        
    pipeline {
    agent {
        node {
            label "linux && java21"
        }
    }

    stages {
        stage("Build") {
            steps {
                echo "Start Build"
                sleep(5)
               sh"./mvnw clean compile test-compile"
                echo"Finish Build"
            }
        }

        stage("Build 2") {
            steps {
                echo "Start Build"
                sh"./mvnw test"
                echo "Finish Build"

            }
        }

        stage("Deploy") {
            steps {
                echo "Hello Deploy 1"
                sleep(5)
                echo "Hello Deploy 2"
                echo "Hello Deploy 3"
                echo "Hello Deploy 4"
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

