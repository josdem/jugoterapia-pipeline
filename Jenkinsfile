#!/usr/bin/env groovy
pipeline {
  agent any
  stages {
    stage('Build Jugoterapia') {
      steps {
        echo 'Building Jugoterapia'
        build job: 'jugoterapia-mobile-debug'
        echo 'Done!'
      }
    }
    stage('Stop Jugoterapia') {
      steps {
        echo 'Stoping Jugoterapia'
        sh 'sudo systemctl stop jugoterapia-webflux'
        echo 'Done!'
      }
    }
    stage ('Start Jugoterapia Webflux Job') {
      steps {
        echo 'Starting Jugoterapia Build Job'
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
