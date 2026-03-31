pipeline {
    agent any

    stages {
        stage('Clone Repo') {
            steps {
                echo 'Cloned successfully'
            }
        }

        stage('Run Docker') {
            steps {
                bat 'docker run hello-world'
            }
        }
    }
}
