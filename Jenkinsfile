pipeline {
    agent any
    tools {
            maven 'Maven'
            jdk 'jdk8'
        }
    stages {
        stage('build') {
            steps {
                sh 'mvn --version'
            }
        }
    }
}