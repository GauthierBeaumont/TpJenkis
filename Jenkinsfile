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
        sh 'rocketeer deploy --host="192.168.33.10" --username="ubuntu" --password="6fe7b5d4f79c9ddd94b4a8f7" --repository="ierBeaumont_TpJenkis_master-VQG3PRE3ZWOYZ3AOY7QNMDPSKCQVEXEK3WP4FKZR6GF7O3R7RSDA" --key=""'
      }
    }
  }
}