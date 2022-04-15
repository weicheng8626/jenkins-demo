node("jenkins-slave") {
    stage('Get a Maven Project') {
        container('jnlp') {
            stage('Maven version') {
                sh 'kubectl get ns'
                sh 'aws configure'
            }
        }
    }
}

