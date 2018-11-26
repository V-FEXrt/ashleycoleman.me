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
        sh 'aws s3 rm s3://$DOMAIN_NAME --recursive'
        sh 'aws s3 cp $WEBSITE_SOURCE_ROOT s3://$DOMAIN_NAME/ --recursive --exclude ".git/*"'
      }
    }
  }
  environment {
    DOMAIN_NAME = 'www.ashleycoleman.me'
    WEBSITE_SOURCE_ROOT = './public/'
  }
}