pipeline {
    agent any
    environment {
        GITHUB_TOKEN = credentials('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')
    }
    stages {
        stage('Checkout') {
            steps {
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
                script {
                    sh '''
                    # Configuring Git
                    git config --global user.email "workspaceaditi832@gmail.com"
                    git config --global user.name "AditiJS"
                    
                    # Deploy to GitHub Pages
                    git remote set-url origin https://${GITHUB_TOKEN}@github.com/AditiJS/AgileLab.git
                    git checkout -b gh-pages
                    git add .
                    git commit -m "Deploy to GitHub Pages"
                    git push origin gh-pages --force
                    '''
                }
            }
        }
    }
    post {
        always {
            cleanWs()
        }
    }
}
