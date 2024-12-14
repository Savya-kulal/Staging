pipeline {
    agent any  // Runs the pipeline on any available agent

    stages {
        stage('Build') {
            steps {
                echo 'Building the application...'
                sh 'echo Build step'  // A placeholder command for build
            }
        }
        
        stage('Test') {
            steps {
                echo 'Running tests...'
                sh 'echo Test step'  // A placeholder command for test
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deploying the application...'
                sh 'echo Deploy step'  // A placeholder command for deploy
            }
        }
    }

    post {
        success {
            echo 'Pipeline completed successfully!'
        }
        failure {
            echo 'Pipeline failed.'
        }
    }
}

