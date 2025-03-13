pipeline {
    agent any

    stages {
        stage('Clone Repository') {
            steps {
                git branch: 'main', url: 'https://github.com/Stefan-R-Petrov/MyApp-semple.git'
            }
        }

        stage('Build') {
            steps {
                echo 'Building the project...'
                // Добави билд команди тук
            }
        }

        stage('Test') {
            steps {
                echo 'Running tests...'
                sh 'echo "Tests passed!"'
            }
        }

        stage('Package') {
            steps {
                echo 'Creating a ZIP package...'
                sh 'zip -r build.zip *'
                archiveArtifacts artifacts: 'build.zip', fingerprint: true
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deploying application...'
                // Добави деплой команди тук
            }
        }
    }
}
