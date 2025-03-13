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
                // Добави реални билд команди тук
            }
        }

        stage('Test') {
            steps {
                echo 'Running tests...'
                script {
                    sh 'echo "Tests passed!"'
                }
            }
        }

        stage('Package') {
            steps {
                echo 'Creating a ZIP package...'
                script {
                    sh 'zip -r build.zip *'
                }
                archiveArtifacts artifacts: 'build.zip', fingerprint: true
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deploying application...'
                // Добави деплой стъпки
            }
        }
    }
}
