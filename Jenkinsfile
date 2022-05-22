#!groovy

pipeline {
  agent none
  stages {
    stage('Start') {
      agent {
        docker {
          image 'image1'
        }
      }
      steps {
        sh 'echo Build running'
      }
    }
    stage('Docker Build') {
      agent any
      steps {
        sh 'docker build -t image1 .'
      }
    }
  }
}