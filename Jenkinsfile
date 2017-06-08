pipeline {
  agent any
  stages {
    stage('git pull') {
      steps {
        sh '''#!/bin/bash
cd /var/www/html/TpJenkis
git pull origin master
'''
      }
    }
  }
}