pipeline {
  agent any
  stages {
    stage('stage 1') {
      parallel {
        stage('stage 1') {
          steps {
            sleep 19
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
            sh './jenkins/testscript'
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