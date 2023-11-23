pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                git 'https://github.com/5454-jay/cclab3.git'
            }
        }

        stage('Build') {
            steps {
                // Run build commands according to your YAML build file
                sh 'npm install'
                sh 'npm run build'
            }
        }

        stage('Deploy') {
            steps {
                // Deploy to your chosen GCP service
                // Example: Copy build files to a GCP bucket or deploy a container
                sh 'gcloud app deploy'
            }
        }
    }
}
