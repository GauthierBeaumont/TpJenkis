pipeline {
  agent any
  stages {
    stage('git pull') {
      steps {
        sh '''#!/bin/bash
cd /var/www/html/TpJenkis
sudo su
git pull origin master
'''
      }
    }
    stage('Composer Update') {
      steps {
        sh '''#!/bin/bash
cd /var/www/html/TpJenkis
composer update'''
      }
    }
  }
}