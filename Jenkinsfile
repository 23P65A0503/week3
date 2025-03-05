pipeline {
  agent any
  stages {
    stage('clone') {
      steps {
        git 'https://github.com/23P65A0503/week3.git'
      }
    }
    stage('Build') {
      steps {
        echo 'Building the project...'
        sh 'javac HelloWorld.java'
      }
    }
    stage('Test') {
      steps {
        echo 'Running tests...'
        sh 'java HelloWorld'
      }
    }
    stage('Deploy') {
      steps {
        echo 'Deploying the project...'
      }
    }
}
  post {
    success {
      echo 'Pipeline completed successfully!'
    }
    failure {
      echo 'Pipeline failed'
    }
  }
}
