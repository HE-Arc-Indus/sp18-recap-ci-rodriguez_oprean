pipeline {
    agent any
    tools {
            maven 'maven'
            jdk 'jdk8'
        }
    stages {
        stage('build') {
            steps {
              sh 'make'
              archiveArtifacts artifacts: '**/target/*.jar', fingerprint: true
            }
        }
        stage('Test') {
            steps {
                sh 'make check || true'
                junit '**/target/*.xml'
            }
        }
    }
    post{
      always {
          archiveArtifacts artifacts: 'build/libs/**/*.jar', fingerprint: true
          junit 'build/reports/**/*.xml'
      }
    }
}