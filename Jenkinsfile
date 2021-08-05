pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Building..'
                sh 'mkdir testdir'
                sh 'cd testdir'
            }
        }
        stage('Test') {
            steps {
                echo 'Testing..'
                sh 'touch hello.txt'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying....'
            }
        }
    }
}
