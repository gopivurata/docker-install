pipeline {
    agent {label 'node'}
    stages {
        stage ('git') {
            steps {
                git branch: 'main', 
                    url: 'https://github.com/gopivurata/docker-install.git'
            }
        }
        stage ('docker-install') {
            steps {
                sh 'cd docker-install'
                sh 'sh docker.sh'
                sh 'docker info'
            }
        }
    }
}