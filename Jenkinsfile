pipeline {
  agent any
  stages {
    stage('Deploy') {
      when {
        expression {
          env.BRANCH_NAME == 'master'
        }

      }
      steps {
        sh 'ls'
      }
    }
  }
  environment {
    DOMAIN_NAME = 'www.ashleycoleman.me'
  }
}