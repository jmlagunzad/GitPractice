pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Building..'
                bat 'mkdir testdir'
                bat 'cd testdir'
            }
        }
        stage('Test') {
            steps {
                echo 'Testing..'
                bat 'touch hello.txt'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying....'
            }
        }
    }
}
