pipeline {
  agent any
  stages {
    stage('stage 1') {
      parallel {
        stage('stage 1') {
          steps {
            sh './jenkins/build.sh'
            archiveArtifacts 'target/startup.jar'
          }
        }
        stage('archive') {
          steps {
            archiveArtifacts './deploy/startup.jar'
          }
        }
      }
    }
    stage('error') {
      parallel {
        stage('error') {
          steps {
            echo 'PRT "hello world"'
          }
        }
        stage('parally') {
          steps {
            sh '''./jenkins/testall.sh

'''
          }
        }
      }
    }
    stage('End') {
      parallel {
        stage('End') {
          steps {
            sleep 2
          }
        }
        stage('error') {
          steps {
            sh 'echo cd '
          }
        }
      }
    }
  }
}