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
        stage('') {
          steps {
            echo 'hello'
          }
        }
      }
    }
    stage('') {
      steps {
        echo 'PRT "hello world"'
      }
    }
  }
}