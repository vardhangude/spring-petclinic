pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                sh './mvnw clean install'
            }
        }

        stage('Test') {
            steps {
                sh './mvnw test'
            }
        }

        stage('Package') {
            steps {
                sh './mvnw package'
            }
        }
        stage('Debug Env') {
            steps {
                sh 'env'
                sh 'whoami'
                sh 'docker --version'
        }
}

    }
}
