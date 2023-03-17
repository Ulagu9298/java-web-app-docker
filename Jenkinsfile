pipeline {
    agent any
    stages {
        stage("pull code"){
            steps {
                git 'https://github.com/Ulagu9298/java-web-app-docker.git'
            }
        }
        stage('build package') {
            steps {
                def mavenHome =  tool name: "Maven-3.5.6", type: "maven"
                def mavenCMD = "${mavenHome}/bin/mvn"
                sh "${mavenCMD} clean package"
            }
        }
    }
}
