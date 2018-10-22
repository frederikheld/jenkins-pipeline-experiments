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
        sh 'git ftp --push ftp://dev.frederikheld.de/deploy/jenkins-pipeline-experiments --username  '
      }
    }
  }
  environment {
    FTP_USER = 'credentials(\'deploy-ftp\')'
    FTP_PW = 'credentials(\'deploy-ftp\')'
  }
}