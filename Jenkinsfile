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
        sh 'script scripts/build2.sh'
      }
    }

    stage('Tests') {
      steps {
        sh '''chmod +x ./scripts/test.sh;
./scripts/test.sh'''
      }
    }

  }
  environment {
    registry = 'lucy21/cicd-pipeline'
  }
}