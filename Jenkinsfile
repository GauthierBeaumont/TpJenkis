pipeline {
  agent any
  stages {
    stage('First') {
      steps {
        sh 'composer update'
        sh 'php artisan key:generate'
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