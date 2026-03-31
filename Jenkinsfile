pipeline {
    agent any

    stages {

        stage('Build Docker Image') {
            steps {
                echo 'Building Docker Image...'
                bat 'docker build -t agile-project .'
            }
        }

        stage('Remove Old Container') {
            steps {
                echo 'Removing old container (if exists)...'
                bat 'docker rm -f mycontainer || exit 0'
            }
        }

        stage('Run Docker Container') {
            steps {
                echo 'Running Docker Container...'
                bat 'docker run -d -p 5000:80 --name mycontainer agile-project'
            }
        }

    }
}
