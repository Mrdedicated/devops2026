pipeline{
    agent any

    stages{
        stage('Build1'){
            steps{

                sh 'sleep 5'
                echo 'First Time Build...'
            }
        }
        stage('Build2'){
            steps{

                sh '''

                #!/bin/bash
                pwd
                ls -ltr
                sleep 5

                '''
                echo 'Second Time Build...'
            }
    }
}