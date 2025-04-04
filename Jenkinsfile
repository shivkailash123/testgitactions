pipeline {
    agent any
    triggers {
        githubPush()  // Automatically triggers on GitHub push
    }
    stages {
        stage('Clone') {
            steps {
                git branch: 'main', url: 'https://github.com/shivkailash123/testgitactions'
            }
        }
        stage('Build') {
            steps {
                sh 'mvn clean install'  // Change if using Gradle or other build tools
            }
        }
        stage('Test') {
            steps {
                sh 'mvn test'
            }
        }
    }
}
