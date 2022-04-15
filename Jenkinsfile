node("jenkins-slave") {
    stage('Get a Maven Project') {
        container('jnlp') {
            stage('Maven version') {
                sh 'aws configure'
                sh 'kubectl get ns'
            }
        }
    }
}

