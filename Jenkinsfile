pipeline {
    agent any
    environment {
        K8S_CONFIG = credentials('jenkins-k8s-config')
    }
    stages {
        stage('Install Kubectl') {
            steps {
                sh 'curl -LO https://dl.k8s.io/release/$(curl -L -s https://dl.k8s.io/release/stable.txt)/bin/linux/amd64/kubectl'
                sh 'chmod +x kubectl'
                sh './kubectl version --client'
            }
        }
    }
}
