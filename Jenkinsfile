pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                // Pull code from GitHub
                git branch: 'main', url: 'https://github.com/vermaatul2946-dotcom/dev4.git'
            }
        }

        stage('Build Docker Image') {
            steps {
                sh 'docker build -t my-project:latest .'
            }
        }

        stage('Run Tests') {
            steps {
                // Replace with your test command if you have tests
                sh 'echo "Running tests..."'
            }
        }

        stage('Deploy Container') {
            steps {
                // Run container on port 5000
                sh 'docker run -d -p 5000:5000 my-project:latest'
            }
        }
    }
}
