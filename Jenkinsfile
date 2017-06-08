pipeline {
  agent any
  stages {
    stage('git pull') {
      steps {
        sh '''#!/bin/bash
cd /var/www/html/TpJenkis
ls -al
sudo composer update
'''
      }
    }
  }
}