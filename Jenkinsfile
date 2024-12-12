pipeline {
    agent any
    stages {
        stage('Checkout') {
            steps {
                git 'https://github.com/clahenry/devsecops-jenkins-k8s-tf-sast-sonarcloud-repo.git'
            }
        }
        stage('Build') {
            steps {
                sh 'mvn install'
            }
        }
        stage('Test') {
            steps {
                sh 'mvn test'
            }
        }
        stage('SAST Scan') {
            steps {
                sh 'mvn clean verify sonar:sonar -Dsonar.projectKey=asghenrywebapp -Dsonar.organization=asghenrywebapp -Dsonar.host.url=https://sonarcloud.io -Dsonar.token=6859f248e1ceb034f08304b68c33c22d8662da78'
            }
        }
    }
}
