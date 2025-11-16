pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                echo "Cloning source code from GitHub..."
                git url: 'https://github.com/ommakhana/java.git'
            }
        }

        stage('Build') {
            steps {
                echo "Building Java project..."
                sh 'javac HelloWorld.java'
            }
        }

        stage('Test') {
            steps {
                echo "Running program..."
                sh 'java HelloWorld'
            }
        }
    }

    post {
        failure {
            echo "Pipeline failed. Check logs for details."
        }
    }
}
