#!groovy

pipeline {
  agent none
  stages {
    stage('Start') {
      agent {
        docker {
          image 'image_new'
        }
      }
      steps {
        sh 'echo Build running'
      }
    }
    stage('Docker Build') {
      agent any
      steps {
        sh 'docker build -t image_new .'
		sh 'docker run -it image_new /bin/bash'
      }
    }
  }
}