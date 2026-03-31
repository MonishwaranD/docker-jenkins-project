pipeline {
    agent any

    stages {
        stage('Clone Repo') {
            steps {
                git 'https://github.com/MonishwaranD/docker-jenkins-project.git'
            }
        }

        stage('Build Docker Image') {
            steps {
                bat 'docker build -t agile-project .'
            }
        }

        stage('Remove Old Container') {
            steps {
                bat 'docker rm -f mycontainer || exit 0'
            }
        }

        stage('Run Docker Container') {
            steps {
                bat 'docker run -d -p 5000:80 --name mycontainer agile-project'
            }
        }
    }
}
