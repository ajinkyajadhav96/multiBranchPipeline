pipeline {
    agent any
    stages {

        stage('Compile') {
            steps {
                sh 'printenv'
            }
        }

        stage('Prepare workspace') {
            steps {
                sh 'ls -alh'
                // checkout scm
                checkout([$class: 'GitSCM', 
                branches: [[name: '*/master']], 
                doGenerateSubmoduleConfigurations: false, 
                extensions: [[$class: 'CleanCheckout']], 
                submoduleCfg: [], 
                userRemoteConfigs: [[credentialsId: '5a381809-9e65-449a-84b4-70805c539333', url: 'https://ajinkyajadhav96@bitbucket.org/ajinkyajadhav96/componentlifecycles.git']]
                ])
            }
        }

        stage('Deployment') {
            steps {
                sh 'ssh root@95.216.198.162 mkdir -p /var/www/temp_deploy'
            }
        }
    }