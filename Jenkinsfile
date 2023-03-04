pipeline {
  agent any
  stages {
    stage('Fetch code') {
      steps {
        git(url: 'https://github.com/rajeebswain/jenkins.git', branch: 'main', poll: true)
      }
    }

    stage('Install Apache') {
      steps {
        sh 'sudo apt install apache2 -y'
      }
    }

    stage('Deploy application') {
      steps {
        sh 'sudo cp -R * /var/www/html'
      }
    }

  }
}