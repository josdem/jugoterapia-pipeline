#!/usr/bin/env groovy
pipeline {
    agent any
    stages {
        stage('Stop') {
            steps {
              echo "Stoping Jugoterapia"
              sh "sudo systemctl stop jugoterapia-webflux"
              echo "Done!"
            }
        }
        stage('Build') {
          steps {
            echo "Copying Jugoterapia package"
            sh "gradle clean build "
            echo "Done!"
          }
        }
        stage('Deploy') {
          steps {
            echo "Copying Jugoterapia package"
            sh "cp ${WORKSPACE}/build/libs/jugoterapia-webflux-0.0.1-SNAPSHOT.jar /opt/jenkins/jugoterapia-webflux-0.0.1-SNAPSHOT.jar"
            echo "Done!"
          }
        }
    }
}
