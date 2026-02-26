pipeline {
    agent any

    stages {
        stage('Clone Repo') {
            steps {
                echo 'Repository cloned'
            }
        }

        stage('Build Backend Image') {
            steps {
                sh 'docker build -t backend-image ./backend'
            }
        }

        stage('Run Backend Container') {
            steps {
                sh 'docker run -d --name backend backend-image || true'
            }
        }
    }
}
