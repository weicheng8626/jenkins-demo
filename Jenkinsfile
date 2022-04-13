node("maven") {
    stage('Get a Maven Project') {
        git 'git@gitee.com:smart-retail-software-service/mc-webapp-service.git'
        container('jnlp') {
            stage('Build a Maven project') {
                sh 'mvn -B clean install'
            }
        }
    }
}

