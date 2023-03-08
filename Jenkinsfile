pipeline {
  agent any
  stages {
    stage('Fetch code from Git') {
      steps {
        git(url: 'https://github.com/rajeebswain/jenkins.git', branch: 'main', poll: true)
      }
    }

  }
}