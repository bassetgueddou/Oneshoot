pipeline {
    agent {
        docker {
            image 'postman/newman'
            args '--entrypoint=""'
        }
    }
    stages {
        stage('Check Newman Version') {
            steps {
                sh 'newman --version'
            }
        }
        stage('Run API Tests') {
            steps {

                sh 'newman run collections/commentaire.postman_collection.json -e environs.postman_collection '
            }
        }
    }
}
