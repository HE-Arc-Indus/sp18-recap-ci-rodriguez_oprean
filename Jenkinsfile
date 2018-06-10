pipeline {
    agent any
    tools {
            maven 'maven'
            jdk 'jdk8'
        }
    stages {
        stage('Build') {
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
      always {
        junit "target/surefire-reports/*.xml"
      }
    }
}