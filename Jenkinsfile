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
      always {
        junit 'target/generated-test-sources/test-annotations/*.xml'
      }
    }
}