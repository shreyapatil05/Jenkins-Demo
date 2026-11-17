
pipeline {
    agent any

    stages {

        // Stage 1: Checkout source code from GitHub
        stage('Checkout') {
            steps {
                git branch: 'main',
                    url: 'https://github.com/shreyapatil05/Jenkins-Demo.git'
            }
        }

        // Stage 2: Compile Java program
        stage('Build') {
            steps {
                echo 'Building Java Application...'
                bat 'javac HelloWorld.java'
            }
        }

        // Stage 3: Run Java program
        stage('Run') {
            steps {
                echo 'Running Java Application...'
                bat 'java HelloWorld'
            }
        }
    }

    post {
        success {
            echo 'Pipeline executed successfully!'
        }

        failure {
            echo 'Pipeline execution failed!'
        }

        always {
            echo 'Jenkins Pipeline execution completed.'
        }
    }
}
