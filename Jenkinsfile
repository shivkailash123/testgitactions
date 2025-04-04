pipeline {
    agent any
    // triggers {
    //     githubPush()  // Automatically triggers on GitHub push
    // }
    echo 'chekcing......'
    stages {
        stage('Clone') {
            steps {
                    echo  'Cloning the repository...'
                git branch: 'main', url: 'https://github.com/shivkailash123/testgitactions'
    
            }
        }
        stage('Build') {
            steps {
                echo '⚙️ Starting the build process...'
                // sh 'mvn clean install'  // Change if using Gradle or other build tools
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
    }
        stage('Test') {
            steps {
                echo '🧪 Running tests...'
                // sh 'mvn test'
            }
        }
    }
    echo 'last testing......'
}
