node("maven") {
    stage('Get a Maven Project') {
        git 'https://github.com/jenkinsci/kubernetes-plugin.git'
        container('jnlp') {
            stage('Build a Maven project') {
                sh 'mvn -B clean install'
            }
        }
    }
}

