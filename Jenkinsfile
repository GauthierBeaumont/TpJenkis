pipeline {
  agent any
  stages {
    stage('First') {
      steps {
        sh 'composer update'
        sh 'cp .env.example .env'
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
    stage('deploy') {
      steps {
        sh 'rocketeer deploy --password="6fe7b5d4f79c9ddd94b4a8f7" --key=""'
      }
    }
  }
}