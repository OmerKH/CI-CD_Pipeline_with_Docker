pipeline {
    agent {
        docker { 
            image 'node:22.14.0-alpine3.21'
            args '--user root'
            }
    }
    stages {

        stage('Checkout') {
            steps {
                 git branch: 'main', url: 'https://github.com/OmerKH/Jenkins-Exercise.git'
            }             
        }
        stage('Build') {
            steps {
                sh 'npm install'
            }
        }
        stage('Run') {
            steps {
            sh 'npm start &'

            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying application...'
            }
        }
    }

}
