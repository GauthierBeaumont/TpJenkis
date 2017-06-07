pipeline {
  agent any
  stages {
    stage('git pull') {
      steps {
        sh '''#!/bin/bash
cd /var/www/html/TpJenkis
sudo git pull origin master
sudo composer update
'''
      }
    }
  }
}