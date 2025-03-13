pipeline {
    agent any

    stages {
        stage('Clone Repository') {
            steps {
                script {
                    checkout scm
                }
            }
        }

        stage('Build') {
            steps {
                echo 'Building the project...'
            }
        }

        stage('Test') {
            steps {
                echo 'Running tests...'
                sh 'echo "Tests passed!"'
            }
        }
    }
}
