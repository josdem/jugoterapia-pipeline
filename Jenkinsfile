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
          build job: 'josdem/jugoterapia-webflux/master'
          echo 'Done!'
        }
      }
    }
}
