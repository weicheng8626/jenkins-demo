node("jenkins-slave") {
    stage('Get a Maven Project') {
        container('jnlp') {
            stage('Maven version') {
                sh 'sleep 600'
                sh 'echo $AWS_ACCESS_KEY_ID'
                sh 'echo $AWS_SECRET_ACCESS_KEY'
                sh 'kubectl get ns'
                sh 'aws configure'
            }
        }
    }
}

