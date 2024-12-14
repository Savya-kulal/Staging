pipeline {
    agent any  // Runs the pipeline on any available agent

    stages {
        stage('Build') {
            steps {
                echo 'Building the application...'
                sh 'mvn clean install'  // Example for building a Maven project
            }
        }
        
        stage('Test') {
            steps {
                echo 'Running tests...'
                sh 'mvn test'  // Example for running tests with Maven
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deploying the application...'
                sh 'scp target/app.jar user@server:/deploy/path'  // Example for deploying the build artifact
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

