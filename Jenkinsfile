pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        echo 'build docker image'
        git(url: 'https://github.com/bdulive/helm-charts.git', branch: 'docker-build', credentialsId: 'githubpat')
      }
    }

  }
}