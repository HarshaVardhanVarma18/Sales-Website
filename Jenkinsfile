pipeline {
    agent any

    stages {
        stage('Clone') {
            steps {
                git branch: 'main', url: 'https://github.com/HarshaVardhanVarma18/Sales-Website.git'
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

        stage('Deploy') {
            steps {
                sh 'docker run -d -p 8081:80 sales-website:latest'
            }
        }
    }
}
