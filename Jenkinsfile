pipeline {
  agent any
  stages {
    stage('git pull') {
      steps {
        sh '''#!/bin/bash
sudo su
cd /var/www/html
chmod 777 -R TpJenkis/

cd TpJenkis
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
    stage('Test Laravel') {
      steps {
        sh '''#!/bin/bash
cd /var/www/html/TpJenkis
./vendor/bin/phpunit'''
      }
    }
  }
}