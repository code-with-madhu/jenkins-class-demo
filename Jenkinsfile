pipeline {
  agent any
  stages {
    stage('Git Checkout') {
      steps {
        git(url: 'https://github.com/code-with-madhu/simple-java-maven-app.git', branch: 'main')
        echo 'This is from build checkouts'
      }
    }

    stage('Build') {
      steps {
        echo 'From Build stage'
      }
    }

    stage('Testing') {
      steps {
        echo 'From Testing'
        sleep 5
      }
    }

    stage('Deployment') {
      steps {
        publishHTML(target: '/reports.html')
      }
    }

  }
}
