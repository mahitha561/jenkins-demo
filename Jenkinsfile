pipeline {
    agent any
    stages {
        stage('Clone') {
            steps {
                git 'https://github.com/username/jenkins-demo.git'
            }
        }
        stage('Build Docker Image') {
            steps {
                sh 'docker build -t myapp .'
            }
        }
        stage('Run Container') {
            steps {
                sh 'docker run -d -p 80:80 myapp'
            }
        }
    }
}
