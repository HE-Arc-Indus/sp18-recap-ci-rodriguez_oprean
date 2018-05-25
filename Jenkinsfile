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
    }
    post{
      always {
        junit "target/surefire-reports/*xml"
      }
    }
}