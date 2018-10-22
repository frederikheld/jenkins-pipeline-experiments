pipeline {
  agent any
  stages {
    stage('Minify') {
      steps {
        sh 'echo "minified js" > mylib.min.js'
      }
    }
    stage('Deploy to FTP') {
      steps {
        echo 'Deploying ...'
      }
    }
  }
}