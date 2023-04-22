pipeline {
  agent any
  stages {
    stage('Git Checkout') {
      steps {
        git(url: 'https://github.com/lune21/cicd-pipeline', branch: 'main', credentialsId: 'github-id')
      }
    }

  }
  environment {
    registry = 'lucy21/cicd-pipeline'
  }
}