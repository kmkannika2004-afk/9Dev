pipeline {
    agent any

    stages {

        stage('Build Docker Image') {
            steps {
                bat 'docker build -t flaskapp .'
            }
        }

        stage('Run Dev Container') {
            steps {
                bat 'docker run -d --name dev-container -p 5003:5000 flaskapp'
            }
        }

        stage('Run Test Container') {
            steps {
                bat 'docker run -d --name test-container -p 5004:5000 flaskapp'
            }
        }
    }
}
