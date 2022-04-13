def label = "mypod-${UUID.randomUUID().toString()}"
podTemplate(label: label, cloud: 'kubernetes', containers: [
    containerTemplate(name: 'maven', image: '124623792426.dkr.ecr.cn-northwest-1.amazonaws.com.cn/jnlp-agent-maven:latest', ttyEnabled: true, command: 'cat'),
]) {
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
