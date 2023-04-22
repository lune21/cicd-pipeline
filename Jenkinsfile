pipeline {
  agent any
  stages {
    stage('Git Checkout') {
      steps {
        git(url: 'https://github.com/lune21/cicd-pipeline', branch: 'main', credentialsId: 'github-id')
      }
    }

    stage('Application build') {
      steps {
        script {
          sh 'chmod +x ./scripts/build.sh'
          sh './scripts/build.sh'
        }
      }
    }

  }
  environment {
    registry = 'lucy21/cicd-pipeline'
  }
}
