pipeline {
  agent any
  stages {
    stage('git pull') {
      steps {
        sh '''#!/bin/bash

cd /var/www/html
sudo chmod 777 -R TpJenkis/
cd TpJenkis
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
    stage('Test Laravel') {
      steps {
        sh '''#!/bin/bash
cd /var/www/html/TpJenkis
./vendor/bin/phpunit'''
      }
    }
  }
}