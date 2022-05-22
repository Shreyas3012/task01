#!groovy

pipeline {
  agent none
  stages {
    stage('Maven Install') {
      agent {
        docker {
          image 'image1'
        }
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