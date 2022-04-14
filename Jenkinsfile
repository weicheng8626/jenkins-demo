node("kubectl") {
    stage('Get a Maven Project') {
        container('jnlp') {
            stage('Maven version') {
                sh 'mvn -v'
            }
        }
    }
}

