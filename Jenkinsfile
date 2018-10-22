pipeline {
  agent any
  stages {
    stage('Build') {
      parallel {
        stage('Build') {
          steps {
            echo 'Building ...'
          }
        }
        stage('added_in_web_ui') {
          steps {
            sh 'echo "added_in_web_ui"'
          }
        }
      }
    }
    stage('Test') {
      steps {
        echo 'Testing ...'
      }
    }
    stage('Deploy') {
      steps {
        echo 'Deploying ...'
      }
    }
  }
}