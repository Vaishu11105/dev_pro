pipeline {
    agent any

    stages {
        stage('stage1') {
            steps {
               git branch: 'master', url:'https://github.com/purushothamkotha963/project.git'
            }
        }

        stage('Build Images') {
            steps {
                bat 'docker-compose build'
            }
        }

        stage('Run Containers') {
            steps {
                bat 'docker-compose up -d'
            }
        }

        stage('Test Containers') {
            steps {
                bat 'docker ps'
            }
        }
    }
}
