#!/usr/bin/env groovy

pipeline {
    agent any

    stages {
        stage('Lint') {
            steps {
                sh 'chef exec rubocop -r cookstyle'
                sh 'chef exec foodcritic -t correctness .'
            }
        }
        stage('Test') {
            steps {
                echo 'Testing..'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying....'
            }
        }
    }
}
