pipeline {
  agent any
  environment {
    FTP_USER = credentials('credentials-deploy-ftp')
    FTP_PW = credentials('credentials-deploy-ftp')
  }
  stages {
    stage('Minify') {
      steps {
        sh 'echo "minified js" > mylib.min.js'
      }
    }
    stage('Deploy to FTP') {
      steps {
        echo 'Deploying ...'
        sh 'curl -T mylib.min.js ftp://dev.frederikheld.de/deploy/jenkins-pipeline-experiments --user $FTP_USER:$FTP_PW'
      }
    }
  }
}
