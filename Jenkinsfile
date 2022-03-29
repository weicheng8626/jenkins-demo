pipeline {
    agent any
    stages {
        stage('Install Kubectl') {
            steps {
                sh 'curl -LO "https://dl.k8s.io/release/$(curl -L -s https://dl.k8s.io/release/stable.txt)/bin/linux/amd64/kubectl"'
                sh 'chmod +x kubectl'
                sh 'mkdir -p ~/.local/bin'
                sh 'mv ./kubectl ~/.local/bin/kubectl'
                sh 'export PATH=$PATH:~/.local/bin/'
                sh 'kubectl version --client'
            }
        }
    }
}
