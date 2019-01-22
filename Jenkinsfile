pipeline {
    agent any
    stages {
        stage('Compile') {
            steps {
                sh 'yarn add package.json'
                sh 'yarn start'
            }
        }
        // stage('Test') {
        //     steps {
        //         sh 'yarn test'
        //         sh 'a'
        //         sh 'q'
        //     }
        // }
        // added 
        stage('Build') {
            steps {
                sh 'yarn build'
            }
        }
    }
}