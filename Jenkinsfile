pipeline {
    agent any

    tools {
        maven 'Maven 3.9.12'
    }

    stages {
        stage('Build') {
            steps {
                echo "compiling start"
               sh 'mvn compile'
            }
        }

        stage('Test') {
            steps {
                echo "testing start"
                sh 'mvn clean test'
            }
        }

        stage('Package') {
            steps {
                echo "packaging start"
                sh 'mvn package'
            }
        }
    }

    post {
        success {
            echo "BUILD SUCCESS 🎉"
        }

        failure {
            echo "BUILD FAILED ❌"
        }
    }
}
