pipeline {
  agent any
  stages {
    stage('stage 1') {
      parallel {
        stage('stage 1') {
          steps {
            sh './jenkins/build.sh'
          }
        }
        stage('stage 3') {
          steps {
            echo 'hello world'
          }
        }
        stage('error') {
          steps {
            echo 'hello'
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
            sh '''./jenkins/build.sh

'''
          }
        }
      }
    }
    stage('End') {
      steps {
        sleep 2
      }
    }
  }
}