pipeline {
    agent any
        tools{
            maven "mymaven"
        }
    stages {
        stage('Code') {
            steps {
                git clone "https://github.com/Bhargavareddykakunuri/Jenkins-End-to-End-Pipeline-project.git"
            }
        }

        stage('Build Artifact') {
            steps {
                sh 'mvn clean package'
            }
        }

        stage('Docker Build') {
            steps {
                sh 'docker build -t employee-app:latest .'
            }
        }

        stage('Deploy Container') {
            steps {
                // Stop old container if exists
                sh 'docker stop employee-container || true'
                sh 'docker rm employee-container || true'
                // Run new container
                sh 'docker run -d --name employee-container -p 8080:8080 employee-app:latest'
            }
        }
    }
}
