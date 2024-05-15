pipeline {
    agent any
    stages {
        stage('Checkout') {
            steps {
                // Clone the repository containing the HTML code
                git 'https://github.com/your-username/your-repo.git'
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
                // Copy the HTML file to the deployment directory
                sh 'cp app.html /var/www/html/'
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
