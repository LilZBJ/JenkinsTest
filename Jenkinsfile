pipeline {
  agent {
    docker {
      image 'composer:latest'
      args '# docker pull composer:latest'
    }

  }
  stages {
    stage('Build') {
      steps {
        sh 'composer install'
      }
    }

    stage('Test') {
      steps {
        sh './vendor/bin/phpunit tests'
      }
    }

  }
}