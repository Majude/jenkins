pipeline {
    agent any

    tools {
        maven 'Maven3' // Use the name from the Jenkins configuration
    }

    stages {
        stage('Clone Repository') {
            steps {
                git branch: 'main', credentialsId: '1f667d93-2b7e-40b0-b22e-50fb68298363', url: 'https://github.com/Majude/jenkins.git'
            }
        }

        stage('Build') {
            steps {
                bat 'mvn clean package' // 'bat' for Windows
            }
        }

        stage('Test') {
            steps {
                bat 'mvn test' // 'bat' for Windows
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

