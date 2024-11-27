pipeline {
    agent {
        docker {
            image 'python:3.10-slim'  // Use a Python image
        }
    }
    environment {
        BROWSER = "chrome"
    }

    stages {
        stage('Checkout') {
            steps {
                sh 'git clone https://github.com/AlexKuznetsov7878/final_jenkins.git'
            }
        }
        stage('Install Dependencies') {
            steps {
                sh 'pip install -r requirements.txt'
            }
        }
        stage('Run Tests') {
            steps {
                sh 'pytest tests/test_google.py'
            }
        }
    }
}
