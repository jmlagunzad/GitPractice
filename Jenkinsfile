pipeline {
    agent any


    environment {
        STRING = 'Vibe check'
    }

    stages {
        stage('Build') {
            steps {
                echo 'Building..'
                bat 'cd testdir'
                input "${STRING}?"
            }
        }
        stage('Test') {
            steps {
                echo 'Testing..'
                if (fileExists('hello.txt') {
                    echo 'hello.txt exists'
                } else {
                    bat 'echo hello.txt'
                }
            }
        }
        stage('Deploy') {
            environment {
                STRING = 'Deploying'
            }
            steps {
                echo "${STRING}...."
            }
        }
    }

    post {
        always {
            echo 'naolways'
        }
        success {
            echo 'Wowie!'
        }
        failure {
            echo 'Me :('
        }
        // unstable {
        //     echo 'This will run only if the run was marked as unstable'
        // }
        // changed {
        //     echo 'This will run only if the state of the Pipeline has changed'
        //     echo 'For example, if the Pipeline was previously failing but is now successful'
        // }
    }
}
