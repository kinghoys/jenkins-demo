pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                git url: 'https://github.com/kinghoys/jenkins-demo.git', branch: 'main'
            }
        }
        
        stage('Build') {
            steps {
                echo 'Building project...'
                bat 'echo Build step for Windows'
            }
        }
        
        stage('Test') {
            steps {
                echo 'Running tests...'
                bat 'echo Test step for Windows'
            }
        }
        
        stage('Deploy') {
            steps {
                echo 'Deploying application...'
                bat 'echo Deploy step for Windows'
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
