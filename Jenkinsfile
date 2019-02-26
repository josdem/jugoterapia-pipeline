#!/usr/bin/env groovy
pipeline {
    agent any
    stages {
        stage('Stop') {
            steps {
              echo "Stoping Jugoterapia!"
              sudo systemctl stop jugoterapia-webflux
              echo "Done!"
            }
        }
    }
}
