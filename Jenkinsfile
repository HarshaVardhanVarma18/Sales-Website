pipeline {
    agent any

    stages {
        stage('Clone Repo') {
            steps {
                git branch: 'main', url: 'https://github.com/HarshaVardhanVarma18/Sales-Website'
            }
        }

        stage('Build') {
            steps {
                sh 'chmod +x build.sh'
                sh './build.sh'
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deployment step (can be Docker run or copy)'
            }
        }
    }
}
