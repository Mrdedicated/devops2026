pipeline{
    agent {
        label 'slave1'
    }

    stages{
        stage('Checkout') {
            steps {
                checkout ([ $class: 'GitSCM',
                            branches: [[name: '*/main']], 
                            extensions: [], 
                            userRemoteConfigs: [[
                                credentialsId: 'Mrdedicated', 
                                url: 'https://github.com/Mrdedicated/devops2026.git'
                            ]]
                        ])
            }
        }
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
}