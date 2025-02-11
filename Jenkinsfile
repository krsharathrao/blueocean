pipeline {
  agent any
  stages {
    stage('fetch code') {
      steps {
        git(url: 'https://github.com/krsharathrao/blueocean.git', branch: 'main')
      }
    }

    stage('install apache & start apache') {
      steps {
        sh '''sh \'\'\'sudo apt install -y apache2 
sudo service apache2 start\'\'\''''
      }
    }

    stage('deploy app') {
      steps {
        sh 'sh \'sudo cp -R * /var/www/html/\''
      }
    }

  }
}