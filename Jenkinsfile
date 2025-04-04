pipeline {
    agent any

    stages {
        stage('Initial Check') {
            steps {
                echo 'Checking......'
            }
        }

        stage('Clone') {
            steps {
                echo 'Cloning the repository...'
                git branch: 'main', url: 'https://github.com/shivkailash123/testgitactions'
            }
        }

        stage('Build') {
            steps {
                echo '⚙️ Starting the build process...'
                // sh 'mvn clean install'  // Uncomment if using Maven
            }
        }

        stage('Display Files') {
            steps {
                script {
                    echo 'Listing files in workspace...'
                    sh 'ls -lah'
                }
            }
        }

        stage('Test') {
            steps {
                echo '🧪 Running tests...'
                // sh 'mvn test'
            }
        }
    }

    post {
        always {
            echo 'Last testing......'
        }
    }
}
