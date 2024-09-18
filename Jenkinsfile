pipeline {
    agent any  // Runs on any available Jenkins agent

    stages {
        stage('Checkout') {  // Stage 1: Checkout code from the repository
            steps {
                git 'https://github.com/kinghoys/jenkins-demo.git'  // Replace with your repo URL
            }
        }
        
        stage('Build') {  // Stage 2: Build the project
            steps {
                echo 'Building project...'
                bat 'mvn clean install'  // Replace with your actual build command (e.g., npm, gradle, etc.) for Windows
            }
        }
        
        stage('Test') {  // Stage 3: Run tests
            steps {
                echo 'Running tests...'
                bat 'mvn test'  // Replace with your testing command for Windows
            }
        }
        
        stage('Deploy') {  // Stage 4: Deploy the project (could be to staging/production)
            steps {
                echo 'Deploying application...'
                // Add deployment script here (e.g., copy files to a server, run a deploy script)
            }
        }
    }
    
    post {
        always {
            echo 'Pipeline completed.'
        }
        success {
            echo 'Pipeline succeeded.'
        }
        failure {
            echo 'Pipeline failed!'
        }
    }
}
