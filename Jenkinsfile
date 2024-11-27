pipeline {
    agent any

    environment {
        BROWSER = "chrome"
    }

    stages {
        stage('Checkout') {
            steps {
                git clone 'https://github.com/AlexKuznetsov7878/final_jenkins.git'
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
