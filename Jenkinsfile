pipeline {
    agent any

    environment {
        BROWSER = "chrome"
    }

    stages {
        stage('Setup Virtual Environment') {
            steps {
                sh '''
                # Use bash explicitly
                bash -c "
                python3 -m venv venv
                source venv/bin/activate
                pip install -r requirements.txt
                "
                '''
            }
        }
        stage('Run Tests') {
            steps {
                sh '''
                # Use bash explicitly for test execution
                bash -c "
                source venv/bin/activate
                pytest tests/test_google.py
                "
                '''
            }
        }
    }
}
