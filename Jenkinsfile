pipeline {
  agent any
  stages {
    stage('Fetch code') {
      steps {
        git(url: 'https://github.com/rajeebswain/jenkins.git', branch: 'main', poll: true)
      }
    }

    stage('Deploye') {
      steps {
        ansiblePlaybook(disableHostKeyChecking: true, playbook: 'install-apache.yml', inventory: 'dev.inv')
      }
    }

  }
}