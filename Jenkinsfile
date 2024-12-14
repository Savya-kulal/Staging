pipeline {
    agent any  // Runs the pipeline on any available agent

    environment {
        // Environment variables, if needed
        APP_NAME = 'SampleApp'
        DEPLOY_PATH = '/deploy/path'
        SERVER_USER = 'user'
        SERVER_HOST = 'your-server.com'
    }

    stages {
        stage('Checkout') {
            steps {
                // Checkout the latest code from the Git repository
                echo 'Checking out the code...'
                git 'https://github.com/Savya-kulal/Staging.git'
            }
        }

        stage('Build') {
            steps {
                // Build the application using Maven
                echo 'Building the application...'
                sh 'mvn clean install'
            }
        }

        stage('Test') {
            steps {
                // Run unit tests using Maven
                echo 'Running tests...'
                sh 'mvn test'
            }
        }

        stage('Deploy') {
            steps {
                // Deploy the application, assuming it is a Java JAR file
                echo 'Deploying the application...'
                sh "scp target/${APP_NAME}.jar ${SERVER_USER}@${SERVER_HOST}:${DEPLOY_PATH}"
            }
        }
    }

    post {
        success {
            echo 'Pipeline succeeded!'
        }
        failure {
            echo 'Pipeline failed!'
        }
        always {
            echo 'Cleaning up...'
            // Any cleanup tasks, if required
        }
    }
}

