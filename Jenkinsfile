pipeline {
    agent any

    stages {
        stage('Clone') {
            steps {
                git 'https://github.com/HarshaVardhanVarma18/Sales-Website.git'
            }
        }

        stage('Build Script') {
            steps {
                sh './build.sh'
            }
        }

        stage('Build Docker Image') {
            steps {
                script {
                    docker.build("sales-website:latest")
                }
            }
        }
    }

    triggers {
        pollSCM('* * * * *')
    }
}
