pipeline {
    agent any
    environment {
        K8S_CONFIG = credentials('aws_iam_credentials')
    }
    stages {
        stage('Build Aws Env') {
            steps {
                sh 'curl "https://awscli.amazonaws.com/awscli-exe-linux-x86_64.zip" -o "awscliv2.zip"'
                sh 'unzip awscliv2.zip'
                sh './aws/install'
                sh 'aws --version'
            }
        }
        
        stage('Install Kubectl') {
            steps {
                sh 'curl -LO https://dl.k8s.io/release/$(curl -L -s https://dl.k8s.io/release/stable.txt)/bin/linux/amd64/kubectl'
                sh 'chmod +x kubectl'
                sh './kubectl version --client'
            }
        }
    }
}
