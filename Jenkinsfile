pipeline {
  agent any
  stages {
    stage('Fetch code') {
      steps {
        git(url: 'https://github.com/krsharathrao/jenkins-demo.git', branch: 'main')
      }
    }

    stage('Install apache') {
      steps {
        sh 'sudo apt install -y apache2'
      }
    }

    stage('deploy code') {
      steps {
        sh 'sudo cp -R * /var/www/html/'
      }
    }

  }
}