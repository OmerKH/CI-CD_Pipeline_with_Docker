pipeline {
    agent {
        docker { 
            image 'node:19-alpine' 
            args '--user root'
            }
    }
    stages {

        stage('Checkout') {
            steps {
                git 'https://github.com/OmerKH/Jenkins-Exercise.git'
            }             
        }
        stage('Build') {
            steps {
                sh 'npm install'
            }
        }
        stage('Run') {
            steps {
                sh 'npm start'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying application...'
            }
        }
    }

}
