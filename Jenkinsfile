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
                // Ако имаш билд команда, добави я тук
            }
        }

        stage('Test') {
            steps {
                echo 'Running tests...'
                script {
                    sh 'echo "Tests passed!"'  // Тестване
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
                // Ако имаш деплой команда, добави я тук
            }
        }
    }
}
