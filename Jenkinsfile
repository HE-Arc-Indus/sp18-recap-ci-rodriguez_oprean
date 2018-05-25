pipeline {
    agent any
    tools {
            maven 'maven'
            jdk 'jdk8'
        }
    stages {
        stage('build') {
            steps {
                sh 'mvn --version'
            }
        }
        stage('Test') {
                    steps {
                        sh 'mvn test'
                    }
                }
    }
    post{
    success {
                     echo 'whole pipeline successful'
                 }
                 failure {
                     echo 'pipeline failed, at least one step failed'
                 }

    }
}