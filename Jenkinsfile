pipeline {
  agent any
  stages {
    stage('Composer Update') {
      steps {
        sh 'composer update'
      }
    }
    stage('Test Laravel') {
      steps {
        sh '''./vendor/bin/phpunit
php artisan cache:clear
./vendor/bin/behat'''
      }
    }
  }
}