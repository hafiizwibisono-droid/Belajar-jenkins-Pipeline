pipeline {
    agent {
        node {
            label "linux" 
        }
    }

    tools {
        jdk 'jdk21' 

    stages {
        stage("Build") {
            steps {
                echo "Start Build with Java 21"
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
                echo "Hello Deploy"
            }
        }
    }

    post {
        always { echo "I will always say Hello again!" }
        success { echo "Yay, success" }
        failure { echo "Oh no, failure" }
    }
 }
}
