pipeline {
    agent any

    stages {
        stage('Clone Repository') {
            steps {
                git 'https://github.com/Majude/jenkins.git'
            }
        }

        stage('Build') {
            steps {
                sh 'mvn clean package' // Change to 'npm install' or 'python setup.py install' if needed
            }
        }

        stage('Test') {
            steps {
                sh 'mvn test' // Change to 'npm test' or 'pytest' if needed
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deploying application...'
                // Add deployment scripts (Docker, SCP, Kubernetes, etc.)
            }
        }
    }
}
