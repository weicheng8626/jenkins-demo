pipeline {
    agent any
    stages {
        stage('Install Kubectl') {
            steps {
                sh """
                    curl -LO https://dl.k8s.io/release/$(curl -L -s https://dl.k8s.io/release/stable.txt)/bin/linux/amd64/kubectl
                    chmod +x kubectl
                    ./kubectl version --client
                """
            }
        }
    }
}
