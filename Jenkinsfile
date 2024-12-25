pipeline {
    agent any 
    stages {
        stage('build stage') {
            steps {
                 checkout scmGit(branches: [[name: '*/main']], extensions: [], userRemoteConfigs: [[credentialsId: 'nn', url: 'https://github.com/Savya-kulal/Staging.git']])
                sh "mvn clean install"
            }
        
        }
    }
}

