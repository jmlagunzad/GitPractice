pipeline {
    agent any


    environment {
        STRING = 'Vibe check'
    }

    stages {
        stage('Build') {
            steps {
                echo 'Building..'
                // dir('C:\\Users\\Jm\\Desktop\\Git Clones\\testdir')
//                 input "${STRING}?"
            }
        }
        stage('Test') {
            steps {
                echo 'Testing..'
                script {
                    if(STRING == 'Vibe check')
                    {
                        echo 'Absolutelay.'
                    }
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
        stage('Parrarel') {
            parallel{
                stage('Hello') {
                    echo 'Hello'
                }
                stage('World') {
                    echo 'World'
                }
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
