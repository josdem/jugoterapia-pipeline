#!/usr/bin/env groovy
pipeline {
  agent any
  stages {
    stage('Stop Jugoterapia') {
      steps {
        echo 'Stoping Jugoterapia'
        sh 'sudo systemctl stop jugoterapia-webflux'
        echo 'Done!'
      }
    }
    stage ('Start Jugoterapia Webflux Job') {
      steps {
        echo 'Stoping Jugoterapia'
        build job: 'jugoterapia-webflux'
        echo 'Done!'
      }
    }
    stage('Start Jugoterapia') {
      steps {
        echo 'Starting Jugoterapia'
        sh 'sudo systemctl start jugoterapia-webflux'
        echo 'Done!'
      }
    }
  }
}
