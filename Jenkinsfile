pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                echo "Branch: ${env.BRANCH_NAME}"
                checkout scm
            }
        }

        stage('Build') {
            steps {
                echo "Building the application..."
                // Example build command:
                sh 'echo Simulating build...'
            }
        }

        stage('Test') {
            steps {
                echo "Running tests..."
                // Example test command:
                sh 'echo Simulating tests...'
            }
        }

        stage('Deploy') {
            when {
                branch 'main'
            }
            steps {
                echo "Deploying to production (main branch only)..."
            }
        }
    }

    post {
        always {
            echo "Pipeline finished for branch: ${env.BRANCH_NAME}"
        }
    }
}
