pipeline {
    agent  any
    }
    parameters {
        choice(
            name: 'ENVIRONMENT', 
            choices: ['dev', 'staging', 'prod'], 
            description: 'Select deployment environment'
        )
    }   
    stages {

        stage('Checkout') {
            steps {
                 git branch: 'main', url: 'https://github.com/OmerKH/CI-CD_Pipeline_with_Docker.git'
            }             
        }
        stage('Build') {
            steps {
                sh 'npm docker-compose build'
            }
        }
        stage('Run') {
            steps {
            sh 'docker-compose up -d'

            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying application...'
            }
        }
    }

}
