pipeline {
    agent any
    stages {
        stage('Env Build') {
            steps {
                sh 'curl -LO "https://dl.k8s.io/release/$(curl -L -s https://dl.k8s.io/release/stable.txt)/bin/linux/amd64/kubectl"'
                sh 'chmod +x kubectl'
                sh 'mkdir -p ~/.local/bin'
                sh 'mv ./kubectl /usr/bin/kubectl'
                sh 'kubectl version --client'
            }
        }
    }
}
