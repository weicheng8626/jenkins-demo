def label = "mypod-${UUID.randomUUID().toString()}"
    node(label) {
        stage('Get a Maven Project') {
            git 'https://github.com/jenkinsci/kubernetes-plugin.git'
            container('maven') {
                stage('Build a Maven project') {
                    sh 'mvn -B clean install'
                }
            }
        }
    }
}
