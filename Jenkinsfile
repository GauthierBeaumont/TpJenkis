pipeline {
  agent any
  stages {
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
./vendor/bin/phpunit
php artisan cache:clear
./vendor/bin/behat'''
      }
    }
  }
}