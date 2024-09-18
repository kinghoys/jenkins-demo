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
                bat 'echo Build step for Windows'  // Basic Windows command for testing
            }
        }
        
        stage('Test') {  // Stage 3: Run tests
            steps {
                echo 'Running tests...'
                bat 'echo Test step for Windows'  // Basic Windows command for testing
            }
        }
        
        stage('Deploy') {  // Stage 4: Deploy the project
            steps {
                echo 'Deploying application...'
                bat 'echo Deploy step for Windows'  // Basic Windows command for testing
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
