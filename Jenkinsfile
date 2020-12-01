pipeline {
    agent any

    stages {
        stage('Prepare') {
            steps {
               echo 'test - art';
               // Install dependencies, create a new .env file and generate a new key, just for testing
               sh "composer install"
               sh "cp .env.example .env"
               sh "php artisan key:generate"
            }
        }
        stage('Test'){
            steps {
                 sh "./vendor/bin/phpunit"
            }
        }
    }
}