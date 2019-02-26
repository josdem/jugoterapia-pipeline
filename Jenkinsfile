#!/usr/bin/env groovy
pipeline {
    agent any
    stages {
        stage('Stoping') {
            steps {
              echo "Stoping Jugoterapia!"
              sh "sudo systemctl stop jugoterapia-webflux"
              echo "Done!"
            }
        }
    }
}
