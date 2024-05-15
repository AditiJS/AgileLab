pipeline {
    agent any
    stages {
        stage('Checkout') {
            steps {
                // Clone the repository containing the HTML code
                git 'https://github.com/AditiJS/AgileLab'
            }
        }
        stage('Build') {
            steps {
                // In this case, there is nothing to build
                echo 'Building the application...'
            }
        }
        stage('Test') {
            steps {
                // If you had tests, you would run them here
                echo 'Running tests...'
            }
        }
        stage('Deploy') {
            steps {
                // No actual deploy step needed as Live Server will serve from the project directory
                echo 'Deploy step: Ensure files are in the right place for Live Server'
            }
        }
    }
    post {
        always {
            // Clean up workspace
            cleanWs()
        }
    }
}
