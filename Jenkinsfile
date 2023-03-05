pipeline {
  agent any
  stages {
    stage('Featch code') {
      steps {
        git(url: 'https://github.com/rajeebswain/jenkins.git', branch: 'main', poll: true)
      }
    }

    stage('Deploy Ansible') {
      steps {
        ansiblePlaybook(playbook: 'install-apache.yml')
      }
    }

  }
}