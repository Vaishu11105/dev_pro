pipeline {
    agent any

    stages {
        stage('stage1') {
            steps {
                checkout scmGit(branches: [[name: '*/main']], extensions: [], userRemoteConfigs: [[credentialsId: 'purush', url: 'https://github.com/purushothamkotha963/project.git']])
            }
        }

        stage('Build Images') {
            steps {
                sh 'docker-compose build'
            }
        }

        stage('Run Containers') {
            steps {
                sh 'docker-compose up -d'
            }
        }

        stage('Test Containers') {
            steps {
                sh 'docker ps'
            }
        }
    }
}
